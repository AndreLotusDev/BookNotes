---
aliases: 
tags: 
date created: sexta-feira, agosto 30º 2024, 2:43:24 am
date modified: sexta-feira, agosto 30º 2024, 2:55:48 am
---
É um "padrão" usado nos projetos corriqueiramente, todavia envolve muitas controversias.

Para que ele serve:
	É uma forma de ter acesso ao container e fazer os acesso de forma manual ou granular.
	Geralmente usado para evitar se dumpar a controller com 300 interfaces que serao utilizadas somente em um metodo.
	Evita de instanciar diretamente milhares de interfaces, chamando elas somente nos lugares que é necessário, fazer isso a controller ter somente uma interface (IServiceProvider).

Quais os problemas que ele introduz:
	Dificulta bastante efetuar testes nas classes que usam essa metodologia.
	É um padrão fortemente desaconselhado, geralmente somente em ocasiões muito especificas.

Exemplo:

```csharp
using Microsoft.AspNetCore.Mvc;

public class MyController : ControllerBase
{
    [HttpGet("do-something")]
    public IActionResult DoSomething()
    {
        var myService = ServiceLocator.GetService<IMyService>();
        myService.DoSomething();
        
        return Ok("Service Executed");
    }
}
```

PS: Considerado por muitos inclusive como um anti pattern.