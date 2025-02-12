---
aliases: 
tags: 
date created: quinta-feira, setembro 5º 2024, 11:22:01 pm
date modified: quinta-feira, setembro 5º 2024, 11:40:15 pm
---
Muito útil para situações onde você precisa usar muitos IFS, e para se respeitar o O de Open Closed Principle você derivas estrategias diferentes para diferentes situações.

![[Pasted image 20240905233051.png]]

Exemplo em código:

Interface da estrategia:

```csharp
public interface IAttackStrategy
{
    void Attack();
}
```

Tipos de estrategia concretas:
```csharp
public class SwordAttack : IAttackStrategy
{
    public void Attack()
    {
        Console.WriteLine("Player swings a sword!");
    }
}

public class BowAttack : IAttackStrategy
{
    public void Attack()
    {
        Console.WriteLine("Player shoots an arrow!");
    }
}

public class MagicAttack : IAttackStrategy
{
    public void Attack()
    {
        Console.WriteLine("Player casts a fireball!");
    }
}
```

Jogador:
```csharp
public class Player
{
    private IAttackStrategy _attackStrategy;

    public void SetAttackStrategy(IAttackStrategy attackStrategy)
    {
        _attackStrategy = attackStrategy;
    }

    public void Attack()
    {
        if (_attackStrategy != null)
        {
            _attackStrategy.Attack();
        }
        else
        {
            Console.WriteLine("No attack strategy selected!");
        }
    }
}
```

Entrypoint:

```csharp
class Program
{
    static void Main(string[] args)
    {
        Player player = new Player();

        // O jogador começa com uma espada
        player.SetAttackStrategy(new SwordAttack());
        player.Attack(); // Output: "Player swings a sword!"

        // O jogador troca para um arco e flecha
        player.SetAttackStrategy(new BowAttack());
        player.Attack(); // Output: "Player shoots an arrow!"

        // O jogador muda para usar magia
        player.SetAttackStrategy(new MagicAttack());
        player.Attack(); // Output: "Player casts a fireball!"
    }
}
```