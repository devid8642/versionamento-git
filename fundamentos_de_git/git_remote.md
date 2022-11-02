# Trabalhando remotamente

## Introdução

Inicialmente foi discutido que o Git se trata de um sistema de versionamento distribuído. Isso significa que podemos manter cópias dos nossos repositórios locais na internet para que outras pessoas possam baixar uma cópia desse repositório, fazer alterações e enviar essas alterações para que nós possamos baixar de volta. Ou seja, entender como o Git funciona de forma distribuída é o primeiro passo para entender como usar o Git para o desenvolvimento de projetos em conjunto.

## git remote

Com o comando `git remote` é possível visualizar todos os repositórios remotos do repositório local que se encontramos. Com `git remote -v` obtemos também as URLs desses repositórios remotos.

## git remote add

O comando `git remote add <nome> <url>` adiciona um novo repo remoto. Esse nome que vem antes da URL serve para indicar o nome que usaremos toda vez que quisermos nos refirir a URL, dessa forma não precisamos ficar escrevendo a URL completa. 

Além de adicionar é possível renomear e remover respectivamente com os comandos: `git remote rename <nome_atual> <novo_nome>` e `git remote remove <nome>`.

## git fetch && git pull

Para baixar os novos trabalhos que estão em algum repositório remoto pode-se usar o comando `git fetch <repo>` . Esse comando irá baixar os novos trabalhos de todos os ramos do repositório remoto em questão e para poder visualizar esses trabalhos o comando que podemos usar é o `git checkout`. Internamente o Git separa as referências de ramos locais e de ramos remotos, para a listagem de ramos locais rode `git branch` e de ramos remotos rode `git branch -r`. O comando `git fetch` armazena todas as alterações que foram feitas remotamente nesses ramos remotos, assim com o `git checkout` podemos averiguar todas essas alterações antes de adicioná-las ao ramo principal local do nosso projeto.

O que o comando `git pull`faz é simplificar esse processo: ele baixa todas as alterações de determinado ramo e automaticamente tenta fazer a mesclagem com o ramo principal. No contexto de trabalho em conjunto no entanto ele não é tão interessante pois surgem muitos conflitos. E ele também desincentiva a revisão de código.

## git push

Caso um repositório remoto não tenha contribuições que você não tenha baixado localmente, você pode enviar novos trabalhos para esse repositório com o comando `git push`. Exemplo de sintaxe: `git push origin master`, isso enviará todas as alterações do seu ramo atual para o ramo master do repositório origin.



