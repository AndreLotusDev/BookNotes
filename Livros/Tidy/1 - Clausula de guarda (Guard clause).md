---
aliases: 
tags: 
date created: Wednesday, February 5th 2025, 2:52:17 pm
date modified: Wednesday, February 5th 2025, 2:58:55 pm
---
Assim como o early return e avoid nested if's (object calisthenics), o guard clause, ou clausula de guarda tem muitas similiaridades com ambos. 

O padrão da clausula de guarda é toda vez que precisamos executar uma função que exige validações a priori, validamos seus principios e encerramos sua execução previamente caso essas validações não estejam em conformidade.

```cs
public void processarPedido(Pedido pedido) {
    if (pedido == null) {
        throw new IllegalArgumentException("Pedido não pode ser nulo!");
    }

    if (pedido.isCancelado()) {
        return;  
    }

    this.logicaSeguinte();
}
```

Outro exemplo feito diretamente por kent beck em uma library open source de queues.

https://github.com/Bogdanp/dramatiq/pull/470