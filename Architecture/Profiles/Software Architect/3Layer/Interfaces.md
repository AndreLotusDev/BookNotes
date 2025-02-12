---
aliases: 
tags: 
date created: segunda-feira, setembro 9º 2024, 10:21:08 pm
date modified: segunda-feira, setembro 9º 2024, 10:44:36 pm
---
Dentro da camada application ou business devemos criar os contratos (interfaces), ao qual classes concretas logo após devem implementar.

Exemplo: 
![[Pasted image 20240909222407.png]]

Também se faz necessário criar as interfaces de persistencia, ao qual seria interfaces que se comunicam com a camada de dados, todavia de uma forma onde se cria um baixo acoplamento entre a camada de negócio e a camada de dados.

PS: Mesmo a interface de repositorio sendo da camada de dados, ela fica hospedada a classe dentro da camada de aplicação/negócio. Geralmente essa camada também é implementada usando o padrão IRepository.

![[Pasted image 20240909223714.png]]
![[Pasted image 20240909223928.png]]

