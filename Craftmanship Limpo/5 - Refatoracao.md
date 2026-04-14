---
aliases:
tags:
date created: Tuesday, April 14th 2026, 6:32:13 pm
date modified: Tuesday, April 14th 2026, 7:00:32 pm
---
Toda refatoração requer que voce entenda que ela nao deve alterar o comportamento do codigo.
Portanto para garantir que o codigo esteja funcionando de forma igual deve se esperar que o codigo tenha uma boa suite de teste.

Algumas refatorações podem ser feitas automaticas com sua IDE.

**Renomear:** nomear as coisas da trabalho, nao tenha medo de renomear variaveis quantas vezes forem necessario.

**Extrair metodo:** Quanto um metodo fica muito grande da para se isolar e separar pequenos pedaços do código, isso é importante para garantir uma maior legibilidade de código.
	- Todo código deve ser escrito como se fosse uma prosa fácil de se ler.
	- Uma funcoa faz uma coisa, quando nenhuma outra funcao pode ser extraida dela. Ou seja, para que todas as suas funcoes facam uma coisa so, voce deve extrair e extrair até que não se possa extrair mais nada.

Ex: if(employeeShouldHaveFullTimeBenefits(employee)) {
    employee.setFullTimeBenefits();
}

Perceba que é como se a gente tivesse lendo uma prosa.

**Extrair variavel:** as vezes temos expressões complexas, e para facilitar a leitura do código, podemos extrair essas expressões para variáveis com nomes mais significativos.

Outro cenário que podemos usar a variavel é criar variaveis explicativas.

boolean isEligibleForEarlyRetirment = employee.age > 60 && employee.salary > 15_000

if(isEligibleForEarlyRetirment) {
    // ...
}


---

A refatoracão não é nada sem os testes. Os testes garantem que a funcionalidade do código permanece a mesma.

Se voce comecar uma serie de refatoracoes grandes, voce precisa garantir que comite cada passo, caso chegue em um beco sem saida ira precisar reverter alguns passos, caso não tenha comitado tera perdido um tempo imenso.