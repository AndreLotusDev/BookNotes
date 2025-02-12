---
aliases: 
tags: 
date created: Monday, August 26th 2024, 8:37:47 pm
date modified: Monday, August 26th 2024, 8:43:08 pm
---
> O Git utilize um sistema hierárquico de configurações para personalizar a experiência do usuário. Cada repositório Git possui uma pasta `.git` que contém um arquivo de configuração local. Esse arquivo armazena opções específicas para aquele projeto, como o nome do usuário, o endereço de e-mail, as preferências de formatação de código e as cores do terminal.

> Ao executar um commando Git, o sistema primeiro consulta as configurações do repositório local. Se encontrar a opção desejada, ela será utilizada. Caso contrário, o Git buscará a configuração global do usuário, que é armazenada em um arquivo separado. As configurações globais são aplicáveis a todos os repositórios Git do usuário, a menos que sejam sobrescritas por configurações locais.

---

Localizacao do arquivo localmente: ./.git/config

Localizacao do arquivo global: ./user/.gitconfig

---

