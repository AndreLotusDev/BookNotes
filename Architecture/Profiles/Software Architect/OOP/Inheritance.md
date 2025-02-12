---
aliases: 
tags: 
date created: quinta-feira, agosto 29º 2024, 7:22:45 pm
date modified: quinta-feira, agosto 29º 2024, 7:34:05 pm
---
Notes: A orientação a objetos gira em torno da herança.

Hoje em dia em sistemas não é tão recomendado usar herança pq ele introduz muito mais colaterais do que beneficios, tendo em vista do design de base que a herança oferta.

Por exemplo, hoje em dia voce pode usar composição e tornar o codigo mais flexivel, com menos colateral, mais ´facil de testar e que introduz menos breaking changes no código do que com herança.

---
Exemplo de herança, sempre leia herança como, é um, exemplo, cachorro é um animal correto (frase com sentido), animal é um cachorro (frase sem sentido, portanto herança não faz sentido).

```csharp
public class Animal
{
    public string Nome { get; set; }
    public int Idade { get; set; }

    public virtual void EmitirSom()
    {
        Console.WriteLine("O animal faz um som!");
    }
}

public class Cachorro : Animal
{
    public void Latir()
    {
        Console.WriteLine("Au au!");
    }

    public override void EmitirSom()
    {
        Console.WriteLine("Au au!");
    }
}

public class Gato : Animal
{
    public void Miar()
    {
        Console.WriteLine("Miau!");
    }

    public override void EmitirSom()
    {
        Console.WriteLine("Miau!");
    }
}
```