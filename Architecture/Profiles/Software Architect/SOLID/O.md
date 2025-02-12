---
aliases: 
tags: 
date created: quinta-feira, agosto 29º 2024, 8:51:00 pm
date modified: sexta-feira, agosto 30º 2024, 1:06:51 am
---
Open Closed Principle

"Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification".

"Entidades de software (classes, módulos, funções, etc) devem estar abertas para extensão, mas fechadas para modificação".

---

Nunca é bom mexer em uma classe que já está em funcionamento e em produção, ficar alterando ela muito menos.

É sempre bom extendar a classe em outra classe do que alterar uma classe já existente.

Sempre tente criar uma classe de base que possa ser herdada pelas demais.
	Ou seja, a classe base está sempre fechada para modificação.
	Todavia pode ser herdada ou composta para adicionar coisas novas.

Também da pra usar metodos de extensão para permitir respeitar o O do SOLID.

Exemplo de extensão da classe string:

```csharp
public static class StringExtensions
{
    public static string ToUpperFirst(this string str)
    {
        if (string.IsNullOrEmpty(str))
            return string.Empty;

        return char.ToUpper(str[0]) + str.Substring(1);
    }

    public static string   
 Reverse(this string str)
    {
        char[] charArray = str.ToCharArray();
        Array.Reverse(charArray);
        return new string(charArray);   

    }
}
```