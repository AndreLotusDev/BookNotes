---
aliases: 
tags: 
date created: sexta-feira, agosto 30º 2024, 3:37:11 am
date modified: segunda-feira, setembro 2º 2024, 8:50:02 am
---
Como identificar um bom codigo ou codigo ruim?

- Quantidades de linhas de codigo.
	- A quantidade em si é muito subjetivo, depende muito de cada situacao.
	- Todavia por exemplo, 5k de linhas na maioria das situacoes é algo que não é aceitável.
- Número de metodos.
	- Sempre evitar god classes, aquelas classes ao qual fazem cinquenta operacoes ao mesmo tempo, sempre respeite o S do solid e tenha classes isoladas.
- Número de classes.
	- Sempre evitar god classes, aquelas classes ao qual fazem cinquenta operacoes ao mesmo tempo, sempre respeite o S do solid e tenha classes isoladas.
- Linhas de codigo por metodo.
	- As vezes o metodo em si está bom, todavia executa muitas coisaas ao mesmo tempo, porque não quebrar em metodos menores?
- Complexidade ciclomática.
	- If encadeado
- Número de estruturas de decisão.
- 
---

Avaliar a expressividade do código

- Escolha os nomes que revelem a intenção.
- Por que existe.
	- Nada de nomes genericos, sempre nomes com proposito final.
- O que faz.
	- No nome do metodo ele tem que explicar o que ele está fazendo.
- Como é usado.
- Use nomes fáceis de se encontrar.
	- Geralmente para se facilitar a busca generalizada.
- Use nomes pronunciáveis.
- Evite siglas ou acrônimos.
	- Se você usar isso para nomear as coisas, somente quem tem noção profunda do profundo e sobre as regras de negócio irão conseguir dar manutenção no sistema.
- Não economize palavras.
	- Não afeta a performance.
- Evite palavras que podem ser variaveis ou palavras reservadas em outras plataformas.
- Evite dar nomes como "doubleValorPromocional", o tipo não precisa estar no nome.
- Evite trocadilhos, não misture idioma, não mescle nomes.
