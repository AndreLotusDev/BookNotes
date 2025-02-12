---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 12:14:18 am
date modified: sexta-feira, setembro 6º 2024, 12:37:24 am
---
Chamada também de arquitetura hexagonal.

Junção de Onion, DDD, Clean, CQRS e tudo mais.

![[Pasted image 20240906002033.png]]

Exige um conhecimento profundo, portanto tem que se atentar antes de simplesmente sair aplicando ela.

Dividimos a arquitetura hexagonal em duas partes, o lado da User Interface que é o lado que o cliente pode interagir com a aplicação, e o lado da infraestrutura, onde podemos conectar elementos de infraestrutura a nossa aplicação, como bancos, filas e etc.

A direção e fluxo desse estilo arquitetural é sempre cliente > infraestrutura > cliente
![[Pasted image 20240906002319.png]]

O nome de arquitetura hexagonal não significa a quantidade máxima e limite de portas que ela pode ter, mas sim que ela pode ter quantas portas forem necessárias.

![[Pasted image 20240906002942.png]]

![[Pasted image 20240906003614.png]]