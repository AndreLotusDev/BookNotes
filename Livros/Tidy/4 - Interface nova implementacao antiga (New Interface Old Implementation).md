---
aliases: 
tags: 
date created: Wednesday, February 5th 2025, 3:15:14 pm
date modified: Wednesday, February 5th 2025, 3:21:48 pm
---
Podemos refatorar as coisas sem introduzir major breaking changes. Sempre que temos uma implementação/interface antiga, podemos wrappar ela dentro de uma interface mais nova e elegante e mantermos sua funcionalidade como padrão, e depois de usar essa nova interface em todos os lugares em vez da implementação antiga podemos finalmente refatoras as coisas sem quebrar.

Exemplo:

- Lógica antiga que armazena logs em arquivos.

```cs
public class OldLogger
{
    public void WriteToLogFile(string message)
    {
        Console.WriteLine($"[OLD LOGGER] Escrevendo em arquivo: {message}");
    }
}
```

- Criamos uma interface nova

```cs
public interface ILogger
{
    void Log(string message);
}
```

- Criamos um adaptador

```cs
public class OldLoggerAdapter : ILogger
{
    private readonly OldLogger _oldLogger;

    public OldLoggerAdapter(OldLogger oldLogger)
    {
        _oldLogger = oldLogger;
    }

    public void Log(string message)
    {
        _oldLogger.WriteToLogFile(message);
    }
}
```

PS: Perceba que criamos uma interface nova, wrapamos a funcionalidade, ela continua a funcionar do mesmo jeito, e iremos ver onde todos os lugares que chamamos o OldLogger e iremos refatorar para chamar OldLoggerAdapter.

- Criamos a injeção de dependência:

```cs
class Program
{
    static void Main(string[] args)
    {
        OldLogger oldLogger = new OldLogger();
        ILogger logger = new OldLoggerAdapter(oldLogger);
    }
}
```

- Depois de refatorado em todos os lugares

```cs
public class ModernLogger : ILogger
{
    public void Log(string message)
    {
        Sink.ToDB($"[MODERN LOGGER] {message}");
    }
}
```

E trocamos a injeção de dependência:

```cs
class Program
{
    static void Main(string[] args)
    {
        ILogger logger = new ModernLogger();
    }
}
```

Com isso refatoramos as coisas sem criar major breaking.