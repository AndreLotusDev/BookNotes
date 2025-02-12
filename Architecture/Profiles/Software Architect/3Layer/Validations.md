---
aliases: 
tags: 
date created: segunda-feira, setembro 9º 2024, 10:53:10 pm
date modified: terça-feira, setembro 10º 2024, 12:20:27 am
---
Sempre antes de persistir algo no banco de dados precisamos verificar se a entidade ou o agregado da entidade está válido.

Classe base de ajuda para executar as validações.

![[Pasted image 20240909230537.png]]

Ai na camada de negócios podemos chamar da seguinte forma.

![[Pasted image 20240909230645.png]]

Ou seja, somente adicionamos ao banco se tudo estiver ok.

Caso precisamos fazer uma validação na camada de business:

![[Pasted image 20240909232759.png]]

Podemos trazer essa coleção de notificação com essa classe aqui, podendo por fim trazer para camada de UI.

![[Pasted image 20240909235519.png]]

![[Pasted image 20240909235749.png]]

![[Pasted image 20240909235948.png]]




