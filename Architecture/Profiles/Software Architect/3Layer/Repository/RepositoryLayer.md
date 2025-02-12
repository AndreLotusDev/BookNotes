---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 11:33:35 am
date modified: terça-feira, setembro 10º 2024, 11:26:55 pm
---
A camada de dados pode ser usada com ou sem ORM, e nela faremos um fraco acoplamento com a camada de negocio, ambas se comunicam entre si com interfaces.

Quando falamos de DDD, o certo é que a camada de acesso aos dados, as entidades que tem lá não necessariamente deveriam ser as exatas mesma classe que usamos na camada de repositorio, mas infelizmente na esmagadora maioria dos projetos que iremos trabalhar iremos encontrar coisas como essa.

Geralmente na repository layer é adequado adicionar a seguinte configuração:

![[Pasted image 20240910223828.png]]

![[Pasted image 20240910225808.png]]