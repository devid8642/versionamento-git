# Fluxo de ramos

## Introdução

Existem muitos fluxos de trabalho possíveis quando se fala em Git, isso é ainda mais verdadeiro quando levamos em consideração projetos que usem o Git de forma distribuída, ou seja, com as versões principais do projeto em um servidor central e cópias desse projeto na máquina de cada desenvolvedor. Abaixo será abordado alguns fluxos de trabalho possíveis.

## Ramos de longa duração

Em projetos complexos que usam Git é possível criar um sistema de ramos de modo a prover *níveis de estabilidade*. No ramo master é mantido o código que foi ou irá para a produção, ou seja, o código que já está pronto. Alguns commits a frente do ramo master nós mantemos um ramo *dev*, nesse ramo é onde estamos testando as novas funcionalidades que foram desenvolvidas antes de ir para o master. E mais a frente do ramo dev nós mantemos vários outros ramos mais curtos que é onde as funcionalidades são desenvolvidas de fato. Assim a visão que temos desse sistema de ramos se parece com isso:

![](imagens/ramos_de_longa_duracao.png)

Partindo do ramo master, quando mais se desce nesse sistema de ramos mais instável é o código que vemos.

## Ramos por tópicos

O fluxo de trabalho com tópicos pode ser usado em projetos de qualquer tamanho e consiste basicamente em criar um ramo para cada desenvolvimento e ir fazendo as mesclagens de três vias a medida que for necessário. Parece óbvio trabalhar assim com o Git mas seria muito difícil fazer isso com muitos outros sistemas de versionamento.

## Ramos remotos

Ramos remotos são como os locais: ponteiros que referenciam algum commit no repositório remoto em questão. Localmente você pode visualizar os ramos remotos executando `git branch -r`. Localmente os ramos remotos são apenas rastreados e não criados de fato, a menos que você especifique. Isso significa que você não pode "entrar" e trabalhar nesses ramos de fato na verdade você pode apenas baixar o que foi feito em cada um desses ramos e adicionar esses trabalhos aos seus próprios ramos locais.

Para fazer a mesclagem de trabalhos realizados em ramos remotos com seus ramos locais execute `git merge <ramo_remoto>`. Se você quiser criar um ramo local que seja uma cópia de um ramo remoto para trabalhar localmente execute `git checkout -b <novo_ramo_local> <ramo_remeto>`. Isso também irá criar o *rastreamento* entre esse ramo local e o ramo remoto, isos significa que tudo que você baixar e mesclar do ramo remoto irá para esse ramo loca. Por exemplo se você executar `git pull` ele irá enviar os novos trabalhos para esse ramo e não para o ramo master, a não ser que você especifique.

## git push

Com o `git push` você pode enviar o trabalho que você fez em algum ramo para um ramo remoto. A sintaxe é: `git push <remote> <ramo_local>:<ramo_remoto>`. 

## git pull

Esse comando basicamente busca qual ramo remoto o ramo local atual está rastreando e executa um `git fetch` e `git merge` adiantando um pouco de trabalho. Em cenários simples pode ser bom, mas deve-se evitar usar esse comando.

## Deletando ramos remotos

Para deletar ramos remotos execute: `git push <remote> -d <nome_do_ramo>`.