# Apagando Branch Remoto

Quando um branch ja serviu seu proposito, ele nao sera mais necessario, precisando ser removido do repositorio local e remoto, para realizar esta acao se utiliza a opcao **_--delete_**. E preciso fazer um push indicando o nome do repositorio remoto a acao de deletar e o nome do branch a ser removido:

```bash
  git push origin --delete nome-do-branch
```

Ha tambem uma forma abreviada para fazer a exclusao, basta substituir a opcao **_--delete_** por **_:_**, o restante permanece igual:

```bash
  git push origin :nome-do-branch
```

Este exemplo tambem vale para remover as tags, substituindo o nome do branch pelo numero da tag.
