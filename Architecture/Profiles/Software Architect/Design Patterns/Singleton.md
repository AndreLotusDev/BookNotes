---
aliases: 
tags: 
date created: terça-feira, setembro 3º 2024, 1:19:53 am
date modified: quarta-feira, setembro 4º 2024, 6:17:48 pm
---
Geralmente é um objeto que dentro dele tem uma instancia dele propria que é privada, e outra para pegar, quando eu pego a primeira vez eu instancio, se nao eu já pego o que já existe.

Quando você precisa criar um objeto que vai ser usado durante todo o lifetime da sua aplicação, ou quando ele precisa ser usado em vários lugares e precisa garantir que só tenha uma instância dele rodando.

Geralmente é muito útil para videogames, por exemplo para quando se esta criando controller que segura os dados do jogo até acontecer o game over, dentro dessa controller temos a vida, pontuação geral e posição do player.

Geralmente considerado por alguns como um anti pattern.

![[Pasted image 20240903012546.png]]