# Tags no Git

## Introdução

O Git possui uma funcionalidade para marcar pontos importantes no histórico de commits. Essa funcionalidade são as tags e elas servem principalmente para marcar versões do projeto no histórico de commits.

## Visualizando tags

Para visualizar as tags já criadas execute `git tag`, se quiser buscar por uma determinada tag execute `git tag -l "<tag>"`.

## Criando Tags

O Git permite a criação de dois tipos de tags: leves e anotadas. Uma tag leve apenas aponta para um commit enquanto que uma tag anotada guarda várias outras informações. As tags anotadas armazenam a versão inteira do projeto daquele commit além de possuem um autor, data e uma mensagem. São quase como um commit uma tag anotada. 

### Criando tags anotadas

Para criar tags anotadas execute `git tag -a <tag> -m "<mensagem>"`, esse comando criará uma tag para o último commit. Se você quiser criar uma tag para um commit específico execute `git tag -a <tag> <hash_do_commit> -m "<mensagem>"`

### Criando tags leves

Para criar uma tag leve basta não usar parâmetro nenhum na criação da tag como por exemplo: `git tag v1.0`.

## Enviando tags para o repo remoto

Após criar tags localmente talvez seja interessante enviar as tags para o repo remoto do seu projeto, para isso execute `git push <repo_remoto> <nome_da_tag>` ou então `git push <repo_remoto> --tags` para enviar todas as tags locais. A partir do momento que você clona algum repo remoto ele já ira baixar todas as tags daquele repo.