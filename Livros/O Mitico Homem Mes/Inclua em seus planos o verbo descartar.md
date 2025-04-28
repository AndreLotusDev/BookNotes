---
aliases: 
tags: 
date created: Wednesday, April 23rd 2025, 6:30:42 pm
date modified: Wednesday, April 23rd 2025, 11:09:19 pm
---
Ha uma prática na engenharia bem comum, a criação de protótipos e modelos ao qual são feitos com uma única finalidade, corroborar uma ideia, quando validada tal ideia o sistema é descartado, lições são aprendidas e por fim um sistema muito mais enxuto e bem construído, afinal ele foi construido sobre alicerces muito mais sólidos aos quais o protótipo foi construído.

Outro problema que se acontece aos montes na engenharia de software é que ok, não á problemas de evitar o descarte, todavia então o primeiro software, muitas das vezes o POC deve-se portanto ser bem construído desde o primeiro dia.

---

É interessante de se aderir o verbo descartar, pois sistemas em seus passos iniciais tem muitas mudanças de planejamento, tendo um sistema piloto pode permitir acoplar essas ideias já se preparando que elas irão ferir ou mudar inerentemente os fundamentos e base, e como é um sistema de teste, podemos aprender com as experiências e lançar um sistema com fundamentações muito melhores.

#### Planeje o sistema para mudanças

Os sistemas devem ser preparado para mudanças, a literatura de design de software fornece diversas alternativas, soluções e ferramentas para essa solução, uma das mais comuns é a criação de interfaces que se comunicam, modularização e o fechamento de contextos e escopos.

#### Planeje a organização para mudanças

Assim como o código pode e deve estar apto para descarte, estruturas sólidas de hierarquia podem ser trocadas por hierarquias flexíveis e bons planos de carreira. Um exemplo é a escada dupla de ascensão profissional da IBM, ao qual pode-se escolher carreira especialista ou generalista focada em soft skills.

#### Um passo adiante e um passo atrás

É interessante de se ver que o autor entende da importância da cobertura de testes, principalmente os automáticos, já que testes manuais, sempre que há uma mudança, melhoria ou correção se há a necessidade de testes de regressão, ao qual testa todo o sistema a fim de garantir que essas novas mudanças não quebram as implementações atuais.

O autor também explica que é normal e os sistemas são suscetíveis a dar dois passos para frente e um para trás, ou seja, você implementa duas funcionalidades e quebra uma existente, corrige dois bugs e introduz um, isso é bem normal, o que não pode acontecer é a relação 1X1, ou seja, corrigir um bug e adicionar um bug, pois isso pode indicar problemas ainda maiores, alto acoplamento, baixa coesão, falta de cobertura de teste, falta de modularidade e entre outras coisas afim que indicam um software de baixa qualidade.