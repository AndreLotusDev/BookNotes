---
aliases: 
tags: 
date created: quinta-feira, agosto 29º 2024, 7:50:03 pm
date modified: quinta-feira, agosto 29º 2024, 8:01:50 pm
---
O encapsulamento é a arte de esconder os metodos que devem ser privados, e expor os metodos publicos, com isso garantindo que cada camada se comunica com a proxima de forma adequada, nao acessando o que é indevido e também não sendo capaz de acessar o que ela deveria acessar.

Um bom exemplo de encapsulamento é quando você chama um metodo lá na camada superior, e devido a black box, você não sabe o que acontece nas camadas inferiores.

Respeitar o encapsulation é muito importante, pois garante facilidade de dar manutenção (sabemos quais metodos e propriedades podemos acessar), garante facilidade para ler o codigo e camadas, e legibilidade (cognitive load).

---

O C# ainda permite ainda maior encapsulamento com diferentes tipos de acessos. Confira aqui.

### Níveis de Acesso

C# oferece os seguintes níveis de acesso:

- **public:** Membros públicos são acessíveis de qualquer lugar onde a classe for visível.
- **private:** Membros privados são acessíveis apenas dentro da classe em que são declarados.
- **protected:** Membros protegidos são acessíveis dentro da classe em que são declarados e em suas classes derivadas.
- **internal:** Membros internos são acessíveis a qualquer tipo no mesmo assembly.
- **protected internal:** Membros protegidos internos são acessíveis a qualquer tipo no mesmo assembly ou em classes derivadas em outros assemblies.