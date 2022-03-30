# Desfazendo **Commits**

Quando se faz alguma alteracao equivocada ou um commit que nao deveria ser realizado, e possivel corrigir utilizando o **_reset_**. Este comando possui variacoes para diferentes efeitos.

## Opcao **checkout**

Se o arquivo que voce modificou ainda nao foi adicionado ao **_staged_**, a alteracao pode ser resetada utilizando o **_checkout_**:

```bash
  git checkout "nome_do_arquivo"
```

## Opcao **HEAD**

Apos adicionar as modificacoes para **_staged_** (depois que realizou o "git add"), e necessario utilizar outro comando, a opcao **_HEAD_**, ela faz com que o arquivo seja removido da fila do **_staged_**, retirando ele da montagem do pacote do commit a ser fechado:

```bash
  git reset HEAD "nome_do_arquivo"
```

## Opcao **--soft**

Utilizando a mesma situacao do exemplo acima, apos voce ter adicionado modificacoes ao statement e realizado o commit, o pacote de alteracoes foi fechado, neste caso o commit precisa ser desfeito. A opcao **_--soft_** vai desfazer o commit e as modificacoes retornarao ao estagio **_staged_**, ou seja, as modificacoes continuarao na fila para montagem do pacote. Para realizar esta acao, a opcao requer a hash de um commit.
OBS: A hash escolhida deve ser sempre de um commit anterior ao commit no qual se deseja resetar, importante ressaltar que todos os commits que estao acima da hash escolhida, serao resetados:

```bash
  git reset --soft asdf65a4sd6f54asdf65a4sdf654asdf
```

## Opcao **--mixed**

A opcao **_--mixed_** tem o efeito semelhante ao **_--soft_**, porem, ele retira as alteracoes do commit do **_staged_** para **_untracked_**, tambem e ncessario passar a hash do commit anterior aquele no qual se deseja fazer o reset:

```bash
  git reset --mixed asdf65a4sd6f54asdf65a4sdf654asdf
```

## Opcao **--hard**

Esta opcao deve ser utilizada com muita cautela, pois ela ira remover tudo o que tinha anterior ao commit como pastas, arquivos, todos os estados, tambem necessita passar um hash de um commit anterior aquele que se deseja resetar:

```bash
  git reset --hard asdf65a4sd6f54asdf65a4sdf654asdf
```

OBS: os hashs utilizados acima nao representam chaves reais
