# Fluxo de ramos

## Introdução

Existem muitos fluxos de trabalho possíveis quando se fala em Git, isso é ainda mais verdadeiro quando levamos em consideração projetos que usem o Git de forma distribuída, ou seja, com as versões principais do projeto em um servidor central e cópias desse projeto na máquina de cada desenvolvedor. Abaixo será abordado alguns fluxos de trabalho possíveis.

## Ramos de longa duração

Em projetos complexos que usam Git é possível criar um sistema de ramos de modo a prover *níveis de estabilidade*. No ramo master é mantido o código que foi ou irá para a produção, ou seja, o código que já está pronto. Alguns commits a frente do ramo master nós mantemos um ramo *dev*, nesse ramo é onde estamos testando as novas funcionalidades que foram desenvolvidas antes de ir para o master. E mais a frente do ramo dev nós mantemos vários outros ramos mais curtos que é onde as funcionalidades são desenvolvidas de fato. Assim a visão que temos desse sistema de ramos se parece com isso:

![](imagens/ramos_de_longa_duracao.png)

Partindo do ramo master, quando mais se desce nesse sistema de ramos mais instável é o código que vemos.

## Ramos por tópicos

O fluxo de trabalho com tópicos pode ser usado em projetos de qualquer tamanho e consiste basicamente em criar um ramo para cada desenvolvimento e ir fazendo as mesclagens de três vias a medida que for necessário. Parece óbvio trabalhar assim com o Git mas seria muito difícil fazer isso com muitos outros sistemas de versionamento.