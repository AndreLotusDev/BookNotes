---
aliases: 
tags: 
date created: Wednesday, February 5th 2025, 2:59:05 pm
date modified: Wednesday, February 5th 2025, 3:03:12 pm
---
Sempre devemos encontrar simetrias e semelhanças, e quando dois códigos fazem coisas parecidas, eles devem sempre na medida do possível serem semelhantes também na estrutura de código.

Exemplo ruim:

```cs
public class ConnectionManager
{
    private string _connectionString;

    public ConnectionManager(string connectionString)
    {
        _connectionString = connectionString;
    }

    public bool Open()
    {
        if (string.IsNullOrEmpty(_connectionString))
        {
            Console.WriteLine("Erro: Conexão inválida");
            return false;
        }

        Console.WriteLine($"Abrindo conexão com: {_connectionString}");
        return true;
    }

    public void Close()
    {
        Console.WriteLine("Fechando conexão agora!");
    }
}
```

Se você observar, ambos códigos são semelhantes, todavia ambos tem estilos diferentes, para abrir uma conexão fazemos validação, enquanto para fechar não, quando fechamos também não disparamos informação semelhante, só sinalizamos que ela foi fechada, mas não exatamente qual conexão foi fechada.

Exemplo ok:

```cs
public class ConnectionManager
{
    private readonly string _connectionString;
    private bool _isConnected;

    public ConnectionManager(string connectionString)
    {
        _connectionString = connectionString;
    }

    public bool Open()
    {
        if (string.IsNullOrEmpty(_connectionString))
        {
            Console.WriteLine("Falha ao abrir conexão: string de conexão inválida.");
            return false;
        }

        Console.WriteLine($"Abrindo conexão com: {_connectionString}");
        _isConnected = true;
        return true;
    }

    public bool Close()
    {
        if (!_isConnected)
        {
            Console.WriteLine("Conexão já está fechada ou nunca foi aberta.");
            return false;
        }

        Console.WriteLine($"Fechando conexão com: {_connectionString}");
        _isConnected = false;
        return true;
    }
}
```

Perceba que agora o código de ambas operações se parecem muito, mesmo que um seja para fechar e outro para abrir, eles mantém semelhanças até em seu modo estrutural, facilitando assim a leitura na hora de dar manutenção.