# Falando Sobre Branchs

Em outras secoes foi citado varias vezes os **_branchs_**.

O que e um branch?

O branch e um ponteiro, que vai apontar a determinados commits, de forma groceira pode se dizer que e uma parte isolada de um repositorio que futuramente podera ser mesclada com outro branch.

O repositorio tem um branch padrao, geralmente nomeado de **_master_** ou **_main_**, ao criar uma novo branch ele vai apontar para o ultimo commit realizado pelo branch no qual ele se deu origiem, um exemplo simples e a criacao de um novo branch a partir do branch main, um novo branch com nome "nova-feature", sera baseado no branch master, contendo tudo que estiver dentro dele, um novo branch tambem pode ser feito apontado para outro commit que nao esteja no main, pode estar em um outro local.

## Por que usar um **_branch_**?

- Modificar o codigo sem alterar o local (branch) principal
- Os branchs podem ser criados e apagados com muita facilidade
- Varias pessoas trabalhando entre os branchs
- Previne conflitos

## Criando um **_branch_**

Existem algumas formas de criar um branch, pode ser atraves do **_git branch nome-do-branch_**:

```bash
  git branch nome-do-branch
```

Desta forma o branch e criado, no entanto e necessario mover para este branch, para mover entre branchs e utilizado o comando **_git checkout nome-do-branch_**:

```bash
  git checkout nome-do-branch
```

Ha uma outra forma mais pratica que cria o branch e move imediatamente para ele:

```bash
  git checkout -b nome-do-branch
```

## Deletando um **_branch_** local

Para deletar um branch e simples, tomando os devidos cuidados, tendo certeza de que ele nao e mais necessario e seu proposito ja foi realizado, primeiramente e interessante listar os branchs, quando aparecer a lista, um asteristico estara indicando a branch utilizada no momento, o comando e simples:

```bash
  git branch
```

o git nao vai permitir que voce delete o branch que voce esta no momento, entao voce precisa fazer o checkout para qualquer branch que voce dejesa NAO excluir. Exemplo, se voce esta e quer deletar o branch "teste", mude para o "main" ou qualquer outro, comando para deletar o branch e o **_git branch -d nome-do-branch_**.
OBS: O branch so sera excluido se voce ja tiver feito o push e o merge para o repositorio remoto (nas proximas secoes o merge sera abordado)

```bash
  git branch -d nome-do-branch
```

se voce nao quiser fazer push e merge deste branch, voce pode forcar o delete mudando a opcao de -d para -D:

```bash
   git branch -D nome-do-branch
```

Desta forma tudo o que tem no branch sera perdido, sempre se certifique de que voce nao tem nada a ser perdido neste branch.

## Excluir um **_branch_** remoto

Para excluir o branch remoto tambem tem duas formas:

```bash
  git push origin --delete nome-do-branch-remoto
```

Como foi abordado em outra secao, origin e o nome do repositorio remoto dado na sua criacao com a opcao delete indicando a exclusao, seguido do nome do branch a ser deletado.

Vale ressaltar mais uma vez, e aqui com mais enfase, tudo dentro deste branch sera perdido, e aqui no caso e o repositorio remoto, inviabilizando totalmente qualquer forma de obter o seu conteudo novamente.

a forma resumida de fazer esta acao e:

```bash
  git push origin :nome-do-branch
```

Se este repositorio ja tiver sido deletado por alguem, pode ocorrer o seguinte erro:

```bash
  error: unable to push to unqualified destination: remoteBranchName The destination refspec neither matches an existing ref on the remote nor begins with refs/, and we are unable to guess a prefix based on the source ref. error: failed to push some refs to 'git@repository_name'
```

Se isso acontecer, voce pode sincronizar a lista de branchs utilizando:

```bash
  git fetch -p
```

A opcao -p quer dizer "prune" (indica remocao). Ao fazer isto, os branchs remotos que ja nao existem mais serao removidos.
