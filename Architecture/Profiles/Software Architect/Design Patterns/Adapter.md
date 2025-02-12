---
aliases: 
tags: 
date created: quarta-feira, setembro 4º 2024, 6:35:18 pm
date modified: quarta-feira, setembro 4º 2024, 6:40:04 pm
---
Permite que o cliente use o adaptador em vez da interface/classe concreta requirida.

![[Pasted image 20240904183634.png]]

Exemplo, precisamos usar o ILogger, mentimos que implementamos o ILogger, mas o ILogger consume o ILogNetMaster.

![[Pasted image 20240904184004.png]]