# Falando Sobre **Git Stash**

O  **_git stash_** guarda modificacoes que ainda nao foram enviadas em um commit, ele guarda essas modificacoes em um arquivo que pode ser chamada em algum momento determinado.

Um exemplo interessante e se voce estiver trabalhando em alguma modicicacao, e por algum motivo seja necessario criar um novo branch, porem, voce nao quer que esta modificacao va junto para o novo branch neste momento, e ai que o **_stash_** entra, essa ultima modificacao realizada, a que aparece listada ao executar o **_git status_**, vai ser guardada em um arquivo separado que o tracker do git nao vai listar, o comando e:

```bash
  git stash
```

Ao realizar o comando, ele vai salvar e indexar o conteudo ao branch atual com um aviso "WIP", que quer dizer "work in progress". Ao criar o novo branch, tendo como base o branch que voce estava trabalhando, agora e possivel adicionar o conteudo que o **_stash_** guardou com o seguinte comando:

```bash
  git stash apply
```

Ao utilizar o **_git diff_**, o conteudo que estava guardado pelo stash vai ser listado, e o arquivo vai voltar para o staged, ou seja, volta a ser trackeado pelo git com as modificacoes que estavam no **_stash_**.

E possivel ter varios **_stashs_**, separa em partes modificacoes que se deseja separar de um commit. Usando o **_git stash list_**, e possivel visualiza-los e seus respctivos branchs:

```bash
  git stash list
```

Esses **_stashs_** vao ficar no sistema ate que voce os remova, para apagar TODOS eles:

```bash
  git stash clear
```
