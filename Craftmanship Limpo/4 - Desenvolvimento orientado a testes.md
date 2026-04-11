---
aliases: 
tags: 
date created: Tuesday, March 31st 2026, 4:08:22 pm
date modified: Thursday, April 9th 2026, 7:04:05 pm
---
# Leis

1 - Criar uma suite de testes que seja tão confiável que tamanha confiança gerada permite refatoração ou pelo menos que seja possivel e passivel um deploy.
2 - O código gerado deve ser desacoplado para que seja fácil de testar (o dominio ser isolado de conexao interface e etc).
3 - Criar ciclos de feedback curtos para criar um ritmo de programação e feedback estável.
4 - O teste e código de produção devem ser desacoplados, como citado acima, todavia com o teste deve ser possível testar as situações de produção também.

PS: Aplicar TDD sem conhecimentos avançados é díficil e pode gerar inclusive frustração.

**Primeira regra:**
Não escreva nenhum codigo de progucao antes de elaborar um teste que falhou devido a falta desse mesmo codigo, ou seja, nunca codar sem ter testes de cobertura, primeiro sempre testes.

No começo pode parecer absurdo, escrever testes antes do código, todavia isso pode escancarar a saúde dos requisitos, afinal com bons requisitos pode se esperar quais são entradas e saidas (validações e etc).

**Segunda regra:**
Não escreva mais testes do que o suficiente para a indentificacao da falha ou para a falha na compillacao. Resolva a falha escrevendo um pouco do codigo de producao.

**Terceira regra:**
Quando o teste falhar, nao escreva mais codigos de producao do que o suficiente para a falha corrente. Depois que o teste for aprovado, escreva mais codigo de teste.

**PS:** Algumas pessoas preferem escrever um pseudo codigo de teste que tem input e output esperado e validar com o codigo de producao se ele realmente vai funcionar.

O autor argumenta que melhor que debuggar é saber que com uma boa suite de testes não há necessidade de debuggar.

**Quarta regra:**
Refatoração constante. Se você não refatorar constantemente sua codebase ela irá onerar ao longo do tempo.
Em fluxos de TDD você não pede tempo para refatorar, refatorar faz parte do processo constante e voce refatora o tempo todo. É parte cultural.
Você deve refatorar assim como lava as mãos.

### Regra do escoteiro

Sempre que estiver num ambiente, sempre devolva ele melhor de que quando pegou.
Se todo mundo fizesse isso, seria um lugar muito melhor.

---

# Documentacao

Os testes servem como uma documentacao viva, afinal se alterar algo e quebrar voce é obrigado a atualizar instantaneamente.

---

# Beneficios

É divertido ou encorajador.
Voce sabe que as coisas funcionam.

---

As pessoas geralmente dizem que testes nao funcionam, mas geralmente por criarem os testes depois de fazer o codigo.

Voce criou o codigo apenas para funcionar, nao o arquitetou, as vezes vez na correria.

Com isso tambem correu o risco de deixar lacunas na cobertura de testes.

Ou seja, uma suite de testes frágil que não garante realmente que os testes funcionam e que ta pronto para receber deploy em produção.

Criar os testes depois é uma prática não ideal, mas é melhor do que nada.

---

# Ciclo

- Voce escreve uma linha codigo de teste, mas nao compila (logicamente).
- Voce escreve uma linha de codigo de producao que faz o teste compilar.
- Voce escreve outra linha de codigo de teste, mas nao compila.
- Voce escreve outra linha de codigo de producao que faz o teste compilar.
- Voce escreve outra linha ou duas de codigo de teste que compila, mas falha na assercao.
- Voce escreve outra linha ou duas de codigo de producao que passa na assercao.

---

# Observacoes

Como o TDD tem um ciclo muito pequeno e isola as pecinhas de software em pequenos pedaços ele pode levar a crença que ele não funciona ou foi feito somente para pequenas demonstrações, mas esse é o exato ponto, isolar as coisas em pequenos pedacinhos é a melhor forma de manter tudo funcionando.

Caso voce fique empacado, voce pode deletar testes e simplifica-los para não ficar preso.
Sempre tente entender tambem bifurcacoes, quando isso acontecer e voce ficar empacado, volte algumas casas atras e tente o outro caminho que voce ignorou.
Sempre tente achar também testes entre testes. Como se fosse lacunas para serem preenchidas.

Todo software é uma maquina de estados finitos.
O importante independente de ser TDD ou BDD é que seu software seja coberto nessas transicoes de estados.