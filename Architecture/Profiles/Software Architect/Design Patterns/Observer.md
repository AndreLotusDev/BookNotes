---
aliases: 
tags: 
date created: quinta-feira, setembro 5º 2024, 11:40:32 pm
date modified: quinta-feira, setembro 5º 2024, 11:44:43 pm
---
Serve para que objetos possam subscrever em outro e serem notificados de quando há alterações em devidos estados.

Muito usado em state management como no Angular e React (RXJS e Redux).

![[Pasted image 20240905234133.png]]

Codigo Exemplo:

Interface IObserver:

```csharp
public interface IObserver
{
    void Update(int health);
}
```

Interface ISubject:

```csharp
public interface ISubject
{
    void RegisterObserver(IObserver observer);
    void RemoveObserver(IObserver observer);
    void NotifyObservers();
}
```

Player:

```csharp
public class Player : ISubject
{
    private List<IObserver> _observers = new List<IObserver>();
    private int _health;

    public int Health
    {
        get => _health;
        set
        {
            _health = value;
            NotifyObservers();
        }
    }

    public void RegisterObserver(IObserver observer)
    {
        _observers.Add(observer);
    }

    public void RemoveObserver(IObserver observer)
    {
        _observers.Remove(observer);
    }

    public void NotifyObservers()
    {
        foreach (var observer in _observers)
        {
            observer.Update(_health);
        }
    }
}
```

Concrete Observer:

```csharp
public class HealthBar : IObserver
{
    public void Update(int health)
    {
        Console.WriteLine($"Health Bar updated: Player health is now {health}.");
    }
}
```

Sistema de aúdio:

```csharp
public class SoundSystem : IObserver
{
    public void Update(int health)
    {
        if (health <= 20)
        {
            Console.WriteLine("Warning: Low health sound is played.");
        }
        else
        {
            Console.WriteLine("Normal health sound is played.");
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
        // Criação do jogador (Sujeito)
        Player player = new Player();

        // Criação dos observadores
        HealthBar healthBar = new HealthBar();
        SoundSystem soundSystem = new SoundSystem();

        // Registrando os observadores no jogador
        player.RegisterObserver(healthBar);
        player.RegisterObserver(soundSystem);

        // Mudando a vida do jogador
        player.Health = 100; // Output: "Health Bar updated: Player health is now 100." "Normal health sound is played."
        player.Health = 15;  // Output: "Health Bar updated: Player health is now 15." "Warning: Low health sound is played."
    }
}
```

Ou seja, toda vez que a vida mudar a UI de health bar irá mudar, todavia o sistema de audio será notificado também e também dará dispatch do audio.