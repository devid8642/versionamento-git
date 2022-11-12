# O básico de ramos no Git

## Introdução

No cenário mais simples de ramos você irá trabalhar em um ramo até que tudo esteja e pronto e o master não vai mudar. Para criar um novo ramo para iniciar um novo trabalho nós podemos executar `git checkout -b <nome_do_ramo>`, isso é equivalente a criar um novo ramo e já trocar para esse ramo. Após realizar todo o trabalho e commitar tudo você pode voltar para o ramo master e fazer a mesclagem, ou seja, trazer todo o trabalho realizado no novo ramo para o ramo master, através do comando `git merge <nome_do_ramo>`. 

Como você não realizou nenhum commit no ramo master, o que o Git vai fazer é simplesmente mover o ponteiro master até o commit que o ponteiro do novo ramo aponta. Com isso todo o trabalho feito estará em master agora e você pode deletar o novo ramo com `git branch -d <nome_do_ramo>`.

## Outro cenário possível

Neste outro cenário considere que você criou um novo ramo para algum trabalho mas ao mesmo tempo alterou também o ramo master, assim ficando com a seguinte situação:

![](imagens/cenario2.png)
Fonte: https://git-scm.com

Agora você quer fazer o merge e por isso troca para o ramo master e executa `git merge iss53`. Ao fazer isso o Git irá perceber que o ramo master e seu ramo de trabalho já não estão mais a mesma linha no histórico de commits e irá buscar então algum commit que seja comum a linha dos dois ramos. Nesse caso é o commit C2. A partir dai o Git inicia um processo de mesclagem chamado *mesclagem em três vias* e o resultado desse processo é um novo commit, que é especial pois tem mais de um pai, nesse caso o commit anterior do ramo iss53 e o commit anterior do ramo master. Esse commit especial é o resultado da mesclagem e é também a quem o ramo master irá referenciar a partir de agora:

![](imagens/mesclagem_de_tres_vias.png)

## Conflitos

Muito comumente durante as mesclagens ocorrem conflitos, isso ocorre muitas vezes poque modificamos a mesma linha em alguns arquivos em ramos diferentes gerando esses conflitos. Quando isso acontece o Git marca nos arquivos esses conflitos da seguinte forma: Acima dos = está o conteúdo do arquivo no ramo que o HEAD aponta, já abaixo está o conteúdo do arquivo do outro ramo. Assim que você apagar esse caracteres que o Git adicionou e resolver todos os conflitos basta dar `git add` nos arquivos conflitantes que automaticamente o Git irá entender.

Após isso execute `git commit` para finalizar a mesclagem.

## Gestão de branches

O comando `git branch` possui algumas opções interessantes:

1. `git branch` lista de forma simples os ramos do seu repo Git. (\* significa o ramo em que você está atualmente)
2. `git branch -v` lista os ramos e o último commit de cada ramo.
3. `git branch --no-merged´ irá listar todos os ramos que não forma mesclados ainda ao ramo em que você está.
4. `git branch --merged` irá listar todos os ramos que já forma mesclados ao ramo em que você está.

Existem outros parâmetros úteis mas esses são os principais.

Ir para: [Fluxos de trabalho com ramos](fluxo_de_ramos.md)
