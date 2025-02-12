---
aliases: 
tags: 
date created: sexta-feira, agosto 30º 2024, 2:08:47 am
date modified: sexta-feira, agosto 30º 2024, 2:21:24 am
---
PS: A propria documentacao da microsoft é bastante suportiva em termos de explicar sobre os ciclos de vida e injecao de dependencia em geral no .NET.

https://learn.microsoft.com/en-us/dotnet/core/extensions/dependency-injection

---

Transient
	A dependencia é criada em cada requisicao de forma exclusiva, geralmente deve ser utilizado em objetos leves, pois como solicitamos um novo objeto toda hora pode se ocorrer perca de performance ao longo do tempo.

Scoped
	Ocorre no inicio de cada nova requisicao, geralmente o mais utilizado para projetos web, geralmente ajuda a poupar muita memoria se comparado com o transient.

Singleton
	Existe somente um objeto, ele é instanciado no startup da aplicacao.
	Lembrando que o singleton armazena o estado para cada requisicao subsequente, geralmente levando a colaterais se usado no lugar incorreto.

PS: Tome nota também que a mistura de um pai com um tipo de lifetime e o filho com outro tipo de lifetime pode introduzir colaterais indesejados na aplicacao.