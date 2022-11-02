# Desfazendo coisas

Uma das vantagens de versionar é poder voltar a estágios anteriores do projeto e recuperar o que já foi modificado. No caso do Git existem muitas opções diferentes para se fazer isso.

## Refazendo um commit

Essa é uma situação muito comum: você fez um commit e esqueceu de adicionar um arquivo ou a mensagem do commit foi escrita de maneira equivocada. Nesse caso é possível refazer o commit com o comando `git commit --amend`.  Após executar esse comando tudo que estiver na área de stage será adicionado no último commit feito, além disso existirá a possibilidade de alterar a mensagem desse commit.

## Removendo um arquivo da stage

As vezes adicionamos arquivos ao stage e queremos removê-lo de lá. Para isso basta executar o comando: `git restore --staged <file>`.

## Desfazendo alterações

Para desfazer alterações em arquivos modificados basta usar o comando `git checkout -- <file>`. Esse comando descarta todas as alterações em um arquivo e faz ele voltar a versão do último commit, **essas alterações são completamente perdidas**.