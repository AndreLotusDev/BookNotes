---
aliases: 
tags: 
date created: quinta-feira, setembro 5º 2024, 10:04:35 am
date modified: quinta-feira, setembro 5º 2024, 11:30:04 pm
---
Esse padrão serve para que o cliente defina os comandos e com isso o executador executa as operações de acordo com o comando selecionado, também pode se guarda em uma pilha a lista de comandos, podendo assim permitir que esses comandos sejam revertidos a posteriori.

Exemplo, uma calculadora que permite 4 opções e que guarda o historico de operações, permitindo assim desfazer as coisas.

![[Pasted image 20240905231541.png]]

Exemplo sendo usado em um jogo de videogame:

```csharp
public interface ICommand
{
    void Execute();
    void Undo();
}
```

```csharp
public class Player
{
    public void MoveForward()
    {
        Console.WriteLine("Player moves forward.");
    }

    public void Attack()
    {
        Console.WriteLine("Player attacks!");
    }

    public void MoveBackward()
    {
        Console.WriteLine("Player moves backward.");
    }
}
```

```csharp
public class MoveForwardCommand : ICommand
{
    private Player _player;

    public MoveForwardCommand(Player player)
    {
        _player = player;
    }

    public void Execute()
    {
        _player.MoveForward();
    }

    public void Undo()
    {
        _player.MoveBackward(); // Desfazer o movimento andando para trás.
    }
}

public class AttackCommand : ICommand
{
    private Player _player;

    public AttackCommand(Player player)
    {
        _player = player;
    }

    public void Execute()
    {
        _player.Attack();
    }

    public void Undo()
    {
        Console.WriteLine("Undoing attack (not applicable).");
    }
}
```

```csharp
public class InputHandler
{
    private Stack<ICommand> _commandHistory = new Stack<ICommand>();

    public void ExecuteCommand(ICommand command)
    {
        command.Execute();
        _commandHistory.Push(command);
    }

    public void UndoLastCommand()
    {
        if (_commandHistory.Count > 0)
        {
            ICommand lastCommand = _commandHistory.Pop();
            lastCommand.Undo();
        }
    }
}
```

Entry point:

```csharp
class Program
{
    static void Main(string[] args)
    {
        Player player = new Player();
        InputHandler inputHandler = new InputHandler();

        // Definindo comandos
        ICommand moveForward = new MoveForwardCommand(player);
        ICommand attack = new AttackCommand(player);

        // Simulando o jogador apertando botões
        inputHandler.ExecuteCommand(moveForward);  // "Player moves forward."
        inputHandler.ExecuteCommand(attack);       // "Player attacks!"

        // Desfazendo o último comando
        inputHandler.UndoLastCommand();            // "Undoing attack (not applicable)."
        inputHandler.UndoLastCommand();            // "Player moves backward."
    }
}
```