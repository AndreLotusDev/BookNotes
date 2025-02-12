---
aliases: 
tags: 
date created: sexta-feira, setembro 6º 2024, 10:20:19 am
date modified: sexta-feira, setembro 6º 2024, 10:55:50 am
---
É um tema relativamente novo e muito em crescimento.

O termo DevOps deriva da junção das palavras desenvolvimento (development) e operações (operations), sendo uma prática de engenharia de software que possui o intuito de unificar o desenvolvimento de software (dev) e a operação de software (ops).

A característica principal do movimento DevOps é defender fortemente a automação e monitoramento em todas as fases da construção do software, da integração, teste, liberação para implantação e gerenciamento de infraestrutura.

DevOps pretende fornecer, em ciclos de desenvolvimento menores, frequência de implantação aumentada, liberações mais seguras, em alinhamento próximo com os objetivos de negócio.

---

![[Pasted image 20240906104745.png]]

Atribuições do lado do DEV:
- Performance da aplicação
	- Devemos sempre diminuir a latência e monitor por ferramentas de APM.
- Analytics do usuário final
	- Monitorar a latência do usuário final e verificar a performance dos dispositivos.
- Qualidade de código
	- Garantir que o deployment não degradará a performance final.
- Erros em nível de código
	- Encontrar erros raizes e críticos e diminuir eles constantemente. 

Atribuições do lado do OPS:
- Disponibilidade da aplicação
	- Garantir que ela esteja sempre o mais próximo de uptime e respeitando o SLA.
- Performance da aplicação
	- Garantir que a infraestrutura solucione os problemas da melhor forma garantindo escalabilidade e performance.
- Reclamações do usuário final.
	- Garantir que possamos corrigir os erros para o usuário final antes mesmo dele ser capaz de reclamar sobre.
- Analise de performance
	- Usar ferramentas de automatização que permitam entender onde a aplicação tem erro de performance.