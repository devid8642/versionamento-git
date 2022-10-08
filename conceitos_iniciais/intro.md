# Introdução ao versionamento
![](images/versionamento.svg)
Fonte: https://bitbucket.org/product/br/version-control-software

## O que é?
Versionamento significa garantir o rastreamento de todas as alterações feitas em arquivos ao longo do tempo. Ou seja, com um versionador adequado é possível armazenar cada alteração feita em um tipo especial de banco de dados e assim criar um controle das versões desses arquivos. Além disso é possível recuperar versões anteriores, caso as novas versões alcançadas não sejam mais tão interessantes. Os arquivos em questão que trataremos aqui serão arquivos de código-fonte de um software, mas é possível utilizar versionamento com outros tipos de arquivos.

Pensando na recuperação de versões anteriores estáveis, o versionamento funciona como uma proteção ao código fonte de erros humanos e de decisões de projeto equivocadas. Além disso, com o versionamento é possível o chamado desenvolvimento simultâneo resolvendo com ordem os conflitos de código quando surgem. Hoje em dia, o versionamento de software é utilizado na grande maioria dos projetos mesmo em projetos pequenos com apenas um desenvolvedor trabalhando nele. 

## Não usar versionamento
O primeiro problema que surge quando decidimos por não versionar um software é que não teremos uma método produtivo de trabalho em equipe, já que sem o versionamento antes optava-se pela técnica do bloqueio de arquivos impedindo um desenvolvedor de trabalhar em um mesmo arquivo que outro desenvolvedor. Existiam também problemas na organização do código, já que muitas funcionalidades já não mais necessárias não eram apagadas com o receio de que poderiam ser utilizadas em outros momentos.

## Versionamento com o Git
![](images/gitLogoWhite.png)

Os softwares responsáveis pelo versionamento de outros softwares são chamados de *Sistemas de Controle de Versão* (VCS). O Git, que é um VCS gratuito e open source, trabalha com versionamento *distribuído*.  Os tipos de VCSs que existem foram discutidos no artigo seguinte, antes disso é interessante listar algumas funcionalidades do Git:

1. Um histórico completo de alterações de todos os arquivos desde o início do projeto. Cada alteração tem um autor, data e hora e uma pequena mensagem informada pelo próprio autor, e outras coisinhas a mais também.
2. Ramificações e mesclagem de ramificações. São justamente essas duas funcionalidades que permitem o trabalho simultâneo com o Git, para cada nova funcionalidade ou correção de bugs cria-se uma ramificação assim isolando o desenvolvimento dessa funcionalidade das outras. Depois com a mesclagem é possível juntar os trabalhos e corrigir conflitos se necessário. Existem muitas metodologias para organizar ramificações em projetos um exemplo é uma metodologia denominada *Git Flow*. 
3. Integração com as metologias DevOps. Com o Git, e outras ferramentas, é possível alcançar uma cultura de desenvolvimento moderna possibilitando software com mais qualidade e manutenibilidade no código.

Ir para: [Entendendo o Git](git.md)

