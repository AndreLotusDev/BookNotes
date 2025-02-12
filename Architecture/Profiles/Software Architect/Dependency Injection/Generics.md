---
aliases: 
tags: 
date created: sexta-feira, agosto 30º 2024, 2:31:22 am
date modified: sexta-feira, agosto 30º 2024, 2:35:30 am
---
O injetor de dependencia container tem por obrigacao dar suporte para tipos genericos, como repositorios.

Exemplo:

```csharp
public interface ICache<T>
{
    void Set(string key, T value);
    T Get(string key);
}
```

```csharp
public class MemoryCache<T> : ICache<T>
{
    private readonly Dictionary<string, T> _cache = new();

    public void Set(string key, T value)
    {
        _cache[key] = value;
    }

    public T Get(string key)
    {
        return _cache.TryGetValue(key, out var value) ? value : default;
    }
}
```

```csharp
public static class DependencyInjectionExtensions
{
    public static IServiceCollection AddMemoryCache(this IServiceCollection services)
    {
        services.AddScoped(typeof(ICache<>), typeof(MemoryCache<>));
        return services;
    }
}
```

Utilizando na controller

```csharp
[ApiController]
[Route("[controller]")]
public class MyController : ControllerBase
{
    private readonly ICache<string> _stringCache;

    public MyController(ICache<string> stringCache)
    {
        _stringCache = stringCache;
    }

    [HttpGet]
    public IActionResult Get()
    {
        _stringCache.Set("message", "Hello from cache!");
        var message = _stringCache.Get("message");
        return Ok(message);
    }
}
```