---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 12:14:39 am
date modified: sexta-feira, setembro 6º 2024, 9:54:39 am
---
Domain Driven Design.

infelizmente muito mal utilizado e muito mal compreendido.

---

Introduzido em 2003 por Eric Evans.

Indicado para aplicações complexas, com muitas entidades e regras de negócio.

Razoavelmente fácil de entender, difícil de entender.

---

Processo de "implementação" do DDD:

- Entender o negócio.
	- Não só simplesmente sair implementando as coisas.
- Extrair a linguagem ubíqua.
	- Evitar a mesma significação usar diferentes palavras.
- Modelagem Estratégia.
- Definir Arquitetura.
- Modelagem Tática.

---

Sobre linguagem ubíqua:

![[Pasted image 20240906093233.png]]

Vocabulário de todos os termos específicos do domínio.
	Nomes, verbos, adjetivos, jargões, apelidos, expressões idiomáticas e advérbios.

Compartilhado por todas as partes envolvidas no projeto.
	Primeiro passo para evitar desentendimentos.

Usadas em todas formas faladas e escritas de comunicação.

Modelagem estratégica:
	Extrair a linguagem ubíqua vai colaborar na visão e entendimento do negócio e como segregar seu domínio em partes menores e responsáveis.
	Para documentar estas segregações responsáveis utilizamos o Mapa de Contextos (Context Map) que pode ser representado através de imagens e uma simples documentação do tipo de relacionamento entre os contextos.
	Cada contexto delimitado possui sua própria linguagem ubíqua, pois em contextos diferentes, os termos podem ter signficados diferentes.

Modelagem tática:
	Aggregate Object:
		uma entidade que é a raiz agregadora de um processo de domínio que envolve mais de uma entidade.
	Domain Model:
		Uma entidade de domínio, possui estados e comportamentos, lógica de negócio, getters e setters AdHoc, etc.
	Value Object:
		Um objeto qeu agrega valor às entidades, não possui identidade e é imutável.
	Factory:
		Classe responsável por construir adequadamente um objeto/entidade.
	Domain Service:
		Serviço de domínio que atende partes do negócio que não se encaixam em entidades específicas, trabalha com diversas entidades, realiza persistência at´raves de repositórios e etc.
	Application Service:
		Serviço de aplicação que orquestra ações disparadas pela camada de apresentação e fornece DTOs para comunicação entre as demais camadas e para consumo da camada de apresentação.
	Repository:
		Uma classe que realiza a persistência das entidades se comunicando diretamente com o meio de acesso aos dados, é utilizado apenas um repositório por agregação
	External Service:
		Serviço externo que realiza a consulta/persistência de informações por meios diversos.