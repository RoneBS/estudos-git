# Utilizando Git Revert

Em algum momento um commit sera enviado para producao e a aplicao ira quebrar, ou algum commit vai se comportar de forma nao esperada, para estes casos o **_git revert_** fara uma uma especie de rollback no repositorio remoto, ele vai apagar o que foi feito neste ultimo commit, o comando precede do hash do commit que se deseja apagar:

```bash
  git revert asdfga6s5d4ftgasdfga65asdfgasdfgqea
```

Apos utilizar o **_git revert_**, ele vai deixar um novo commit com um log demonstrando que fez acao, ao selecionar a hash que o revert fez e utilizar o **_git show numero-do-hash_**, sera mostrado o conteudo que foi apagado referente ao commit que foi revertido.

```bash
  git show sdf654654sdfgsdfgsdfg9kgjsdlfkjg
```

Vale ressaltar que o commit que foi feito o **_git revert_** ira permanecer no log do git, ele nao e removido mesmo tendo feito essa operacao.
