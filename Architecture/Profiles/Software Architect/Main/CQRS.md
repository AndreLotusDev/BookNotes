---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 12:37:20 am
date modified: sexta-feira, setembro 6º 2024, 1:12:54 am
---
CQRS - Command Query Responsibility Segregation.

Um padrão arquitetural onde o foco principal é separar os meios de leitura e escrita de dados. Alterações de dados são realizados via Commands e leitura de dados são realizados via Queries.

O objetivo do CQRS é prover expressividade para aplicação, pois todos os Commands representam uma intenção de negócio.
	Ex: AumentarSalarioFuncionarioCommand

CQRS promove a consistência eventual, que é quando possuímos um banco de leitura e outro de escrita com os mesmos dados, porém os dados não são consistidos exatamente no mesmo momento.

Muito aplicado em arquitetura hexagonais, microservices ou em aplicações que possuem uma alta demanda de consumo de dados.

Commands:
	Representam uma intenção de mudança de estado de uma entidade. São expressivos e representam uma única intenção de negócio.

Queries:
	É a forma de obter dados de um banco ou origem de dados para atender as necessidades da aplicação.

Todo comando executado dentro de um CQRS deve retornar um evento, independente se for um evento de sucesso ou falha.

O banco que recebe a escrita não necessariamente precisa ser o mesmo banco que o banco de leitura, ambos não precisam ser iguais.

![[Pasted image 20240906010757.png]]