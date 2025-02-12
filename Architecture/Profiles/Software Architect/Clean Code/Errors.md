---
aliases: 
tags: 
date created: segunda-feira, setembro 2º 2024, 9:17:58 am
date modified: terça-feira, setembro 3º 2024, 12:27:40 am
---
Geralmente tratamento de erro se torna bem especifico dependendo da linguagem, plataforma e framework, todavia existem algumas coisas genéricas que podem ser pontuadas.

- Tratar e prever possíveis exceções é de responsabilidade do desenvolvedor.
	- Exceptions não tratadas podem travar e matar a aplicação, por isso todo desenvolvedor deve ter em mente isso.
	- Não encher o código de try catch.
	- Use try catchs globais para evitar de ter que fazer a metodologia acima.
		- Filtros, interceptions, middlewares.
- Retorne exceptions e não código de erro.
- Informe o máximo que puder em sua exception.
	- Por exemplo, no .NET temos o stack trace que mostra o caminho percorrido pelo erro.
- Se necessário crie exceptions personalizadas para um problema específico.
- Não retorne null. é má pratica.

- Regra dos escoteiros: 
	- "Deixe a área de acampamentos mais limpa de como você a encontrou."