---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 11:22:59 am
date modified: segunda-feira, setembro 9º 2024, 10:46:05 pm
---
A arquitetura de 3 camadas é uma das arquiteturas mais simples, todavia não confunda sua simplicidade com a capacidade dela de atender os problemas das empresas.

Simplicidade != qualidade.

---

DDD e 3 Camadas não são a mesma coisa.

3 camadas são a distribuição do trabalho em camada.

DDD é uma filosofia e jeito de pensar em como desenvolver um software onde a modelagem de dominion e entender o negocio seja o centro de tudo, em nenhum momento ele define regras concretas e muito menos quantas camadas um projeto DDD precisa ter.

---

Geralmente pegamos as entidades se formos respeitar o DDD começando pelo agregado, portanto se temos uma entidade pessoa e precisamos pegar um endereço, pegamos sempre o endereço pelo ID da pessoa.

