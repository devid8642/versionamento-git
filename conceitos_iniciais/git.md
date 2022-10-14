# Git

## Introdução

O Git não é simplesmente um versionador de software, ele é um mini sistema de arquivos. Os outros VCSs trabalham armazenando, a cada nova versão, uma lista com as mudanças feitas nos arquivos. Ou seja, eles armazenam os "deltas" entre um arquivo em uma versão e o mesmo arquivo em outra. 

![](images/deltas.png)
Fonte: https://git-scm.com

O Git adota um modelo diferente, ele armazena, a cada versão, os arquivos (ele por inteiro não só o delta) que foram alterados. E se o arquivo não foi alterado ele armazena um link que aponta para a última versão do arquivo.

![](images/git.png)
Fonte: https://git-scm.com

## Identificando alterações
A forma como o Git identifica e registra alterações é usando criptografia SHA-1. A partir do conteúdo de um arquivo o Git, usando esse algoritmo, é capaz de calcular uma sequência de 40 caracteres, essa sequência é chamada de *hash*, que representa o conteúdo do arquivo, pois qualquer alteração que seja feita após o recálculo faz o hash mudar. Mais sobre funções de hash: https://cryptobook.nakov.com/cryptographic-hash-functions

## As Três Áreas

Para utilizar o Git é preciso ter noção de três áreas que o Git possibilita que o seus arquivos estejam: o repositório do Git, a área de trabalho e a área de preparo. Na área de trabalho é o onde você geralmente fica em um projeto e é onde você edita os seus arquivos. Esses arquivos são uma cópia de determinada versão de arquivos que estão no banco de dados do Git. Quando você altera esses arquivos você pode enviá-los para a área de preparado, que é basicamente uma área intermediária entre a área de trabalho e o repositório Git. Quando você termina de preparar todos os arquivos que foram editados você pode finalmente enviá-los para o banco de dados do repositório Git, que é onde eles estarão salvos representando uma nova versão do projeto.

![](images/areas.png)
Fonte: https://git-scm.com

Como pode ser visto na imagem acima, quando da área de preparo nós enviamos novas versões de arquivos para o repositório Git dizemos que fizemos um *commit*. Essa palavra é muito importante e representa um comando do Git.

## Como usar o Git?

A melhor forma de usar o Git é na linha de comando, já que é a única forma de realmente rodar todos os comandos do Git. Portanto deste ponto em diante você precisa saber como usar a linha comando do seu sistema operacional para entender bem o que fazer. Para instalar o Git em seu computador veja: https://git-scm.com/downloads. É muito interessante configurá-lo: https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup.

Ir para: [Fundamentos de Git](../fundamentos_de_git/comandos_basicos.md)