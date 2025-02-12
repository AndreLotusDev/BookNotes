---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 12:11:17 am
date modified: sexta-feira, setembro 6º 2024, 12:18:51 am
---
Arquitetura cebola ou clean architecture.

É um estilo arquitetural e um padrão arquitetural ao mesmo tempo.

![[Pasted image 20240906001413.png]]

A direção de dependencia é sempre o de cima depende do baixo, portanto uma entidade de dominio não depende do repositorio, o repositorio nao depende do negocio e o negocio nao depende da client.

Não confunda sua simplicidade com ela ser ruim, ela atende muitas dos problemas que geralmente as aplicações sofrem.