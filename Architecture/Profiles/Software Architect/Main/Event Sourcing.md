---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 12:14:32 am
date modified: sexta-feira, setembro 6º 2024, 1:16:34 am
---
Nós podemos buscar o estado de uma aplicação para encontrar o estado atual do mundo, e isso responde muitas perguntas. Entretanto há momentos que nós não só queremos ver onde nós estamos, mas também queremos saber como chegamos lá. - Martin Fowler

Permite o replay e navegar entre estados da aplicação.

"Event Sourcing" assegura que todas as mudanças feitas no estado de uma aplicação são armazenadas como uma sequência de eventos. Não só podemos buscar esses eventos, mas também podemos usar este log de eventos para reconstruir estados passados e ajustar automaticamente o estado atual com mudanças retroativas - Martin Fowler

A ideia central é persistir todos os estados anteriores de uma entidade de negócio desde o momento de sua criação. Com este dados em é possível realizar o "replay" dos fatos passados para entender o comportamento do usuário, trabalhar com Big Data, Machine Learning, realizar teste de integração com cenários reais ou simplesmente recriar as entidades se necessário.
