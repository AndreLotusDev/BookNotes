---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 11:33:25 am
date modified: segunda-feira, setembro 9º 2024, 10:24:22 pm
---
Na camada de aplicação ou camada de negocio podemos e devemos colocar as regras de negócio ao que tange aos projetos de 3 camadas, e nele é muito comum usar enumeradores para declarar tipos, isso quando os tipos são bem estritos e raramente irão mudar, caso contrário deixamos dentro do banco.

Nessa camada deve se ter as validações das entidades, por exemplo, quantos digitos um CPF deve ter, se um CNPJ é requerido, etc e etc.

Nessa camada devemos lançar retornos e objetos invalidos, e nunca lançar exceptions de forma direta, isso se da pq exceptions é algo fora do nosso controle ou algo próximo disso, objetos e campos invalidados são coisas que esperamos que o usuário irá inputar de forma errada e precisamos retornar para ele para que ele faça os ajustes necessários.

Fora que, exceptions custam caro. Gerar objetos ricos, no backend, com stacktrace, com informações detalhas etc e etc custa muito caro para o backend.

![[Pasted image 20240909220848.png]]

PS: Existem várias formas de se executar uma validação, podemos criar uma validação do 0, ou podemos consumir algo pré pronto, tudo vai depender do desenvolvedor.
	Podemos usar por exemplo o FluentValidation, que nós ajuda e muito a validar as coisas.
	Por estar na camada de business só nós devemos a atentar de que estamos adicionando uma dependencia a um pacote, ai temos a opção ou de criar essa dependencia ou fazer tudo na mão, mas se for levar em consideração que o fluent validation existe a decadas e que dificilmente irá ser deprecado, é muito melhor utilizar ele do que ficar fazendo as validações na mão.

[[Interfaces]]