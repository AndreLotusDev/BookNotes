---
aliases: 
tags: 
date created: quinta-feira, setembro 5º 2024, 11:49:36 pm
date modified: sexta-feira, setembro 6º 2024, 12:03:25 am
---
Um estilo arquitetural é uma abordagem de como projetar e entregar uma aplicação.

Trata-se de como organizar os componentes responsáveis de uma arquitetura, como eles irão interagir entre si e quais os aspectos tecnológicos irão atender.

Estilos Arquiteturais:
- Arquitetura Monolítica
	- Tudo fica dentro da mesma aplicação, somente tendo um banco desacoplado.
		- Uma arquitetura bem defasada, existem outras opções, todavia não é porque existem outras opções que dependendo do seu contexto de software ela não seja a ideal.
- Arquitetura em camadas
	- Voce divide as responsabilidades de uma aplicação por camadas, como camada de apresentação, controller, de contratos, de negocio e de acesso aos dados.
- Arquitetura REST
	- Separa a forma que a gente escreve nossas APIS.
- Arquitetura em microserviços
	- A maioria das aplicações não precisam ser construídas em microserviços, todavia é excelente para aplicações de grande porte que precisam escalar brutalmente, usamos essa estrategia e separamos nossa aplicação por mini serviços que estão embutidos no mesmo contexto.
	- Nunca pense somente nos beneficios, por mais que os microserviços ajudem e muito a facilitar uma aplicação a escalar, ele atrapalha e muito aumentando exponencialmente a dificuldade de dar manutenção, intercomunicação e simplicidade de entender um sistema (não existe bala de prata).
- SOA x Microserviços
	- No SOA temos serviços que cada um toma parte de um lado do negocio e que eles comunicam entre si.
	- Nos Microserviço temos o mesmo estilo, todavia um SOA pode ser vários microserviços, ou seja, ainda mais granular.
- Plugin Architecture
	- O wordpress é uma arquitetura em plugin
	- ![[Pasted image 20240906000039.png]]
- Client Server Architecture
	- ![[Pasted image 20240906000233.png]]
- Pipes and Filters Architecture
	- ![[Pasted image 20240906000248.png]]