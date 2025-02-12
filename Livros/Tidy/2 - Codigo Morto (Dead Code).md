---
aliases: 
tags: 
date created: Wednesday, February 5th 2025, 2:45:37 pm
date modified: Wednesday, February 5th 2025, 2:49:09 pm
---
Kent Beck explica que não há necessidade de código morto no nosso code base, de certa forma não devemos ter código com 0 usos no nosso code base, com exceção de reflection code, então devemos por etapas ir removendo aos poucos esse código morto que nunca foi usado.

- Nunca remover tudo de uma vez.
- Tomar em consideração que se uma IDE aponta 0 usos de uma função variável ou qualquer outra coisa não significa que de verdade não esteja em uso, pode estar sendo usado em forma de reflection.
- Dado o caso acima, nunca é bom remover tudo de uma vez, é sempre bom ir removendo aos poucos.
- Você não precisa ter dó e piedade do código você pode remove-lo a qualquer hora, afinal ele fica salvo no GIT através do histórico.
- Antes de tentar remover qualquer coisa, mesmo que aos poucos, você pode adicionar tidy protetivo, você pode simplesmente adicionar logs, depurar e avaliar primariamente o que de fato é código morto ou falso positivo.
