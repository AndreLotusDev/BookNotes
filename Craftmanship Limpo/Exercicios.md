---
aliases: 
tags: 
date created: Tuesday, March 31st 2026, 4:48:07 pm
date modified: Wednesday, April 15th 2026, 9:29:15 am
---
# Mini exercicios

- Executar um fluxo de TDD igual especificado no livro (pag.41 - 56).
	- Documentar o processo.
	- Implementar o FIFO.
	- Implementar um verificador de primos.
	- Implementar um jogo de boliche usando TDD. (X)
- Implementar uma suite de testes que teste o dominio com um banco fake e uma com a implementacao real (pagina 152).
- Implementar a premissa de transformacao prioritaria (TPP) (pagina 186).
- Implementar testes de aceitacao (pagina 251).
	- Fitnesse, JBehave, SPecFlow, Cucumber.
- Verificar como um bom fluxo de implementacao por toggle para a feature so subir quando terminada (pagina 343).
- Executar testes de mutacao.

# Maiores exercicios

- Criar um projeto contido em .net core ao qual isolo cada camada, e recebo uma tarefa e outra tarefa que quebre a primeira, e me explique como seria o passo a passo de fazer a tarefa, inclusive começando com os testes, como seria os micro commit e como eu faria para a proxima tarefa que quebraria a primeira.
	- Use o chat gpt (deep thinking) para criar um documento de passo a passo.
	- Defina também como devem ser os criterios de testes, os criterios de aceite.
	- O projeto deve ter uma camada de dominio com agregate root e etc.
	- Como seria a estruturacao para guardar os documentos? sliced architecture? ai poderia guardar os testes de aceite?
	- Explicar como executar bem minuciosamente com passo a passo.
		- Inclusive como seria com o metodo original que voce cria uma linha, nao compila, entao cria o codigo compila e etc. [[4 - Desenvolvimento orientado a testes]] (CICLOS)
	- Incluir um cenario que apos o termino das duas features exigir uma refatoracao tanto no codigo de teste quando no codigo de producao para incluir melhorias.
- Como criar uma camada de dominio tao isolada do restante que seja possivel criar testes facilmente para ela.