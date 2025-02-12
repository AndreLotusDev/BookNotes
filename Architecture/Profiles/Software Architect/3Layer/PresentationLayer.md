---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 11:33:16 am
date modified: quarta-feira, setembro 11º 2024, 1:32:31 am
---
Na camada de apresentação nunca devemos mostrar as entidades da camada de dominio diretamente, sempre devemos usar intermediarios que fazem o filtro de quais fields mostrar na UI, isso ajuda em performance, segurança, legibilidade, manutenção e outros fatores.

Portanto existe as classes de entidade, os DTOS/ViewModel e eles servem para coisas diferentes.

E tem também que isso ajuda na separação de concerns, a lógica aplicada para mostrar na UI nem sempre vai ser a mesma lógica que a lógica de negócio, portanto faz sentido ter essa separação. E se ainda por cima a lógica do viewmodel for algo muito complexo, provavelmente exigirá metodos complexos de muitas linhas que não fazem sentido estar na camada de negócio.

As validações de ViewModel são totalmente diferentes das validações de regra de negócio.

---

Geralmente o pessoal esquece que temos a opção de na camada de apresentação injetar nos metodos de somente leitura a camada de repositorio direto, sem a necessidade de passar pela camada de negocio, isso se da ao fato de que por somente estar lendo os dados que estão no banco de dados não há necessidade nenhuma de colocar uma camada adicional intermediadora.