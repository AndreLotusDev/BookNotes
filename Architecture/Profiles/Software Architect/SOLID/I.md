---
aliases: 
tags: 
date created: sexta-feira, agosto 30º 2024, 1:27:42 am
date modified: sexta-feira, agosto 30º 2024, 1:36:25 am
---
Interface Segregation Principle.

"States that no client should be forced to depend on methods it does not use".

"Clientes não devem ser forçados a depender de métodos que não usam".

Muitas interfaces específicas são melhores do que uma interface única.

---

Maior exemplo disso são as operações de CRUD de banco, em vez de usar somente uma interface você pode separar entre interface de leitura e entrada.
	Por exemplo, em vez de usar IRepository
		Use um IReadRepository, IInsertRepository

Dica: Nunca acumule muitas funções e metodos dentro de uma interface, segregue em interfaces menores.