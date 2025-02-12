---
aliases: 
tags: 
date created: quinta-feira, agosto 29º 2024, 7:35:00 pm
date modified: quinta-feira, agosto 29º 2024, 7:40:38 pm
---
A abstração é o pilar da herança a objetos ao qual diz que devemos introduzir interfaces em prol de reduzir acoplamento entre classes, por exemplo, temos vários tipos de banco de dados, MongoDB, PostgreSQL, MySQL, mas todos eles tem CRUD operation, em vez de consumir eles diretamente por meio da classe deles, eu posso introduzir uma interface em comum em cada um deles e nas classes que dependem de um banco eu consumo a interface (abstração) em vez da classe concreta.

```csharp
// Interface para definir o contrato de uma forma geométrica
public interface IFormaGeometrica
{
    double CalcularArea();
}

// Classe abstrata para representar uma forma geométrica
public abstract class FormaGeometrica : IFormaGeometrica
{
    public abstract double CalcularArea(); // Método abstrato a ser implementado nas classes derivadas
}

// Classe concreta representando um círculo
public class Circulo : FormaGeometrica
{
    public double Raio { get; set; }

    public override double CalcularArea()
    {
        return Math.PI * Math.Pow(Raio, 2);
    }
}

// Classe concreta representando um retângulo
public class Retangulo : FormaGeometri[ca
{]()
    public double Base { get; set; }
    public double Altura { get; set; }

    public override double CalcularArea()
    {
        return Base * Altura;
    }
}
```

Também podemos pensar a abstração como um super classe base que todas as outras classes dependem dela.

OBS: Pode ver que as classes abstratas, ou interfaces (abstrações), não possuem implementação concreta ou rigída, por isso o nome abstração.