---
aliases: 
tags: 
date created: segunda-feira, setembro 2º 2024, 8:50:17 am
date modified: segunda-feira, setembro 2º 2024, 9:12:11 am
---
- Nome de classes devem ser substantivos e não devem conter verbos.
- Nomes de metódos devem conter verbos de preferencia no infinitivo.
	- Ex: AdicionarClient.
- Não use nomes genericos.
	- Ex: Processa(); //Processa oq?
	- Calcula(); //Calcula oq?
- A primeira regra dos métodos é que eles devem ser pequenos. A segunda regra é que eles devem ser menores ainda - Uncle Bob.
	- Método <= 20 linhas.
	- Linha <= 100 caracteres.
	- Classe <= 500 linhas.
- Extraia trechos em métodos privados. (Para que outras camadas não possam ver o que elas não deveriam).
- Métodos devem fazer apenas uma coisa, faze-la certa e somente faze-la.
- Evite muitos parâmetros.
- Não deixe o metódo mentir dizendo que faz uma coisa e faz outras "escondidas".
	- Sempre quebre em metodos menores se necessário.
- Se o método tiver mais de uma responsabilidade, extraia em dois ou mais.
- Leia seu método de cima para baixo como uma narrativa, ele deve fazer sentido.
- Aplique uma boa indentação.