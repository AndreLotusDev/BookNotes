---
aliases: 
tags: 
date created: sexta-feira, agosto 30º 2024, 2:56:14 am
date modified: sexta-feira, agosto 30º 2024, 3:09:13 am
---
Geralmente muitas das vezes quando temos uma interface servindo de derivacao para varias classes concretas temos um problema no design de codigo, ainda mais quando se trata de injecao de dependencia.

Ha tambem que tendo multiplas classes que deriavem de uma mesma interface, se ha a necessidade de acessar os servicos por key, o que implica o consumo do service locator, ou seja, tem que ter muito cuidado ao tomar a decisao de se utilizar desse "approach".

Tomando em consideracao, mesmo com esses dois adendos voce ainda precisa implementar isso, o Simple Injector por exemplo fornece caminhos e alternativas para isso.

Exemplo:

Configuracao

```csharp
public class Startup
{
    private Container _container = new Container();

    public void ConfigureServices(IServiceCollection services)
    {
        services.AddControllers();

        _container.Options.DefaultScopedLifestyle = new AsyncScopedLifestyle();
        services.AddSimpleInjector(_container, options =>
        {
            options.AddAspNetCore()
                   .AddControllerActivation();
        });

        // Registro dos serviços com suas chaves
        ServiceLocator.Configure(_container);
        ServiceLocator.RegisterService<MyServiceA>("A");
        ServiceLocator.RegisterService<MyServiceB>("B");

        // Registro dos tipos no Simple Injector
        _container.Register<MyServiceA>();
        _container.Register<MyServiceB>();
    }

    public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
    {
        app.UseSimpleInjector(_container);
        _container.Verify();
    }
}

```

```csharp
public static class ServiceLocator
{
    private static readonly Dictionary<string, Type> _services = new();
    private static Container _container;

    public static void Configure(Container container)
    {
        _container = container;
    }

    public static void RegisterService<T>(string key) where T : class, IMyService
    {
        _services[key] = typeof(T);
    }

    public static IMyService GetService(string key)
    {
        if (_services.ContainsKey(key))
        {
            return (IMyService) _container.GetInstance(_services[key]);
        }

        throw new ArgumentException("Invalid service key");
    }
}
```

```csharp
using Microsoft.AspNetCore.Mvc;

public class MyController : ControllerBase
{
    [HttpGet("do-something/{key}")]
    public IActionResult DoSomething(string key)
    {
        try
        {
            var myService = ServiceLocator.GetService(key);
            myService.DoSomething();
            return Ok($"Service {key} Executed");
        }
        catch (ArgumentException ex)
        {
            return BadRequest(ex.Message);
        }
    }
}
```