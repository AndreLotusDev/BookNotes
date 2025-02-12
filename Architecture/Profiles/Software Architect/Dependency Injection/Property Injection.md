---
aliases: 
tags: 
date created: sexta-feira, agosto 30º 2024, 2:35:50 am
date modified: sexta-feira, agosto 30º 2024, 2:39:27 am
---
É possível de injetar interfaces por metodos diretamente, é um metodo nao recomendável mas possivel de ser feito.

Exemplo:

```csharp
public interface IMyService
{
    void DoSomething(IMyDependency dependency);
}

public class MyService : IMyService
{
    private readonly IServiceProvider _serviceProvider;

    public MyService(IServiceProvider serviceProvider)   

    {
        _serviceProvider = serviceProvider;
    }

    public void DoSomething(IMyDependency   
 dependency)
    {
        // ...
        // Use a dependência aqui
        // ...
    }

    public void DoSomethingWithResolvedDependency()
    {
        var dependency = _serviceProvider.GetRequiredService<IMyDependency>();
        DoSomething(dependency);
    }
}
```

Outro exemplo usando data attribute:

```csharp
[ApiController]
[Route("[controller]")]
public class MyController : ControllerBase
{
    private readonly IMyService _myService;

    public MyController(IMyService   
 myService)
    {
        _myService = myService;
    }

    [HttpGet]
    public IActionResult   
 GetSomething([FromServices] IAnotherService anotherService)
    {
        // Utilize both _myService and anotherService
        var result = _myService.DoSomething(anotherService.GetData());
        return Ok(result);
    }
}
```