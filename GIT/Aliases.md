---
aliases: 
tags: 
date created: Monday, August 26th 2024, 8:36:27 pm
date modified: Tuesday, August 27th 2024, 5:50:55 pm
---
O git permite que voce gere aliases para commandos, com isso permitindo que o fluxo de trabalho seja menos oneroso ao longo dia, evitando assim digitacao excessiva.

Por exemplo, um .gitconfig com aliases muito utéis:

```
[alias] 
	co = checkout 
	br = branch 
	ci = commit 
	st = status 
	lg = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%reset %s %Cgreen(%cr) %C(bold blue)<%an>%creset' --abbrev-commit ac = add . && commit -m
```

Com essa lista de aliases, por exemplo, para navegar para a main seria necessário somente dar o git co master.

---

PS: Existe alguns sites/links que podem te ajudar a configurar sua lista de aliases para poder te ajudar no flow diário:

https://github.com/GitAlias/gitalias
https://www.durdn.com/blog/2012/11/22/must-have-git-aliases-advanced-examples/
https://gist.github.com/mwhite/6887990