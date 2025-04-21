---
aliases: 
tags: 
date created: Wednesday, April 16th 2025, 9:39:28 am
date modified: Wednesday, April 16th 2025, 10:21:57 am
---
A arquitetura de software se for analisada por livros, é díficil de se manter atual, isso se da, pois, tecnologia é algo que está sempre em mudança, e o mais curioso que cada nova ferramenta as vezes acaba surgindo ou para solucionar um problema atual, ou para substituir uma ferramenta ao qual existe, por exemplo, antes do terraform e kubernetes o mundo se existia por chef e puppet, e assim por seguinte, portanto se apegar a tecnologias em especifico pode ser um erro.

Também pode se analisar que as decisões arquiteturais do momento são baseado na cultura da empresa, política e o que elas podem usar, então entender o contexto é muito importante para entender tais implementações.

Por exemplo, a dez anos atrás muitas empresas de tecnologia passavam por fusões, portanto a maioria das empresas era orientada por serviço e orientada a orquestração.

---

É importante para um bom arquiteto documentar a decisão, por quais motivos tomaram tal decisão, isso ao ponto de vista de governança é muito importante.
	Pode se utilizar ADR para isso (Architectural Decision Record). Geralmente eles utilizam formato markdown, e são armazenados em um repositório de controle de versão ou em uma wiki ou confluence da vida.

Outro ponto importante do lado da governança é definir bons fitness functions, com isso facilita e alinha a expectativa do produto com o lado técnico, exemplos de fitness functions: 
- Performance: O sistema deve suportar 1000 requisições por segundo.

