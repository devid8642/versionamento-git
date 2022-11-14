# Git Rebase

## Introdução

Existem duas formas de integrar o trabalho realizado entre ramos: com o merge e com o rebase. Já tratamos do merge, agora iremos falar do rebase. O rebase pode ser utilizado basicamente nas mesmas situações em que se utilizaria o merge, ou seja, se tivermos por exemplo commits de ramos diferentes divergindo. Nesse caso se você executasse `git rebase <ramo>` todas as alterações que foram introduzidas nesse ramo serão transferidas para o ramo atual. O resultado disso será outro commit, e no seu diretório de trabalho você terá o trabalho do seu ramo e do ramo que sofreu rebasing.

Após o merge entre o outro ramo e esse o resultado prático não difere entre o merge e o rebase, apenas o histórico de commits se torna mais linear. É útil quando por exemplo você está trabalhando com um projeto que você não mantém e você quer enviar o seu trabalho em um histórico linear de commits para uma revisão e mesclagem mais simples.

## Problemas com o rebase

A regra geral é: Não faça rebase de commits que existam fora do seu repo. Se esses commits estão foram do seu repo, outros desenvolvedores já os baixaram e os mesclaram nas suas máquinas locais. Com isso após o seu rebase e push, quando eles baixarem esse trabalho e forem enviar de novo, os commits que você executou um rebasing estarão de novo no histórico de commits, e muitos commits estarão com data, hora e autor duplicados. Ou seja, o histórico de commits será uma confusão total.