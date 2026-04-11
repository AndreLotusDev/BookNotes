---
aliases: 
tags: 
date created: Wednesday, April 9th 2025, 8:02:10 pm
date modified: Thursday, April 10th 2025, 6:23:48 pm
---
As ferramentas de IA são fantásticas, elas permitem que desenvolvedores entreguem código mais rápido.

Atiçam a criatividade, pois removem o bloqueio criativo inicial permitindo a quebra de inércia muito mais rápido, o bloqueio criativo é uma das piores coisas para os programadores.

Elas permitem que o programador entre em estado de flow mais rapidamente, tendo em vista que tudo está no mesmo lugar dentro da mesma IDE, em contraste de por exemplo ter que sair da IDE e entrar no stack overflow para achar a solução.

Claro que nem tudo são flores, IA's não possuem consciência e por isso sempre precisa ser revisado o código gerado que ela produz.

Ela não produz a mesma capacidade de um compilador, ou seja, pode gerar código não compilável.

Por mais que o chat gpt seja excelente para tarefas em geral, usar playground, como por exemplo, do open ai, permite gerar mais especificidade, controle fino e portanto receber uma resposta mais direcionada.

Como toda IA de fato não possui consciencia, é importante realizar alguns benchmarks, temos diversos benchmarks para diversos tipos de situações diferentes, como por exemplo, o bert score... Ao qual avalia o quão próximo as LLM podem gerar código natural.

Entender e prover contexto para as IA's é de suma importância, todavia a engenharia de prompt encontra alguns problemas:
- LLMS são prolixos, portanto se faz necessário pedir que ele seja conciso e direto ao ponto.
- Cada LLM funciona de um jeito, portanto um PROMPT que funciona em uma pode não funcionar em outra.
- Quanto maior a resposta, maior risco dela falhar, o sistema de atenção geralmente começa a falhar em contextos longos e longas cadeias de caracteres.
- Ser claro é fundamental, como LLM não possuem consciencia, sempre evite ambiguidade.

Um PROMPT geralmente é composto por quatro partes:
- Contexto
- Instrucoes para o LLM
- Entrada de contexto
- Formato

Os LLMS podem nos ajudar a traduzir nosso software, claro que é importante depois ter um avaliador linguistico para revisar as saidas das LLMs.

Pode ser util utilizar ao final do prompt palavras auxiliares, ao qual guiam como deve ser a resposta final do LLM.

Sempre tome cuidado para não criar induções em suas perguntas, pois isso pode envenenar tua saida de resposta da LLM:
	- Não é verdade que microserviços melhoram a escalabilidade das aplicações?

Por mais que IA's tenham suas limitações e pontos de melhorias, não existe motivo para se usar ela em momentos certos e contextos especificos, por exemplo, usar o copilot tem se provado muito eficaz, como na AMD, Shopify e Accenture.

Assim como segurança está em alta no mundo todo, o copilot tem investido nisso constantemente, sua plataforma tem varredura de código inseguro, verificar se a inserção de tokens e chaves dentro do codebase e sempre monitora notificando os desenvolvedores sobre essas falhas de segurança.

---

### Páginas

- 81: Como evitar alucinações.
- 85: Sobre agentes.

---

### Exercicios

- Entender os modelos transformers
- Entender a arquitetura generativa adversarias
- Compreender as nuances e diferenças entre o BERT e CHAT GPT
- Utilizar o playground da open ai
- Entender mais sobre engenharia de PROMPT
- Estudar sobre Chain of Thought (CoT)
- Estudar sobre RAG e como implementar um
- Pesquisar como melhorar o uso do github copilot
	- Ver inclusive os comandos de atalho
- Criar um perfil desenvolvedor para eu no chat gpt
- Criar um diagrama e mandar para o chat gpt pedindo para trasnformar um documento formal de analise de requisitos funcionais e nao funcionais
- Usar o Chat GPT para documentar um PRD e SRS
- Ver ferramentas que gerem analise no PR, mensagem do PR e sugestões pro PR
- Pesquisar sobre IA que geram layouts de HTML, inclusive baseado em imagem
- Pesquisar sobre IA que ajudam na escrita e que muda o tom de escrita, como por exemplo grammarly
- Pesquisar sobre IA que geram mini aplicativos sozinhas

---

### Ferramentas

- Replit
- Cody
- Warp
- Bito AI
- Code Llama
- Hugging Face
- Plugin Recombinant IA
- Screenshot to Code GPT
- Claude
- Perplexity
- Github docs