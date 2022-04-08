# O que e **Rebase**?

E semelhante ao merge, ele fara a mescla, porem, com algumas diferencas pontuais:

- Nao vai gerar um novo commit indicando a mescla
- Pode alterar o historico do branch com algumas opcoes
- Leva o commit ao topo do fluxo

O **_rebase_** deve ser usado com muita cautela, por ser bastante poderoso, pode modificar muito o historico do repositorio e precisa ser utilizado por profissionais experintes.

Para fazer o **_rebase_** segue a mesma logica do **_merge_**, se faz o checkout para o branch que quer receber o conteudo de outro branch, no caso de um branch feature necessitar ser mesclado ao main:

```bash
  git rebase feature
```

OBS: No caso acima, e imortante se certificar de que se esta no branch main, ou seja, ter certeza que se esta no branch que vai receber o conteudo do outro branch.
