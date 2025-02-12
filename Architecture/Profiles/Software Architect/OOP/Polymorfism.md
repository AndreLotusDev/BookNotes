---
aliases: 
tags: 
date created: quinta-feira, agosto 29º 2024, 7:47:53 pm
date modified: quinta-feira, agosto 29º 2024, 7:49:17 pm
---
Quando temos uma classe base por causa da orientação a objetos, usamos o polimorfismo, o polimorfismo nada mais é que um objeto/classe que tem comportamentos diferentes baseado no mesmo metodo função.

```csharp
public class Animal
{
    public virtual void FazerSom()
    {
        Console.WriteLine("O animal faz um som.");
    }
}

public class Cachorro : Animal
{
    public override void FazerSom()
    {
        Console.WriteLine("Au au!");
    }
}

public class Gato : Animal
    {
    public override void FazerSom()
    {
        Console.WriteLine("Miau!");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Animal[] animais = { new Cachorro(), new Gato() };

        foreach (Animal animal in animais)
        {
            animal.FazerSom();
        }
    }
}
```