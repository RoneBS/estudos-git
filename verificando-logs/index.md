# Verificando **Logs**

Para verificar como andam os commits feitos no seu repositorio, voce pode visualizar atraves de um log

```bash
  git log
```

Este comando vai mostrar um log dos commits realizados, ele contem:

1.  uma hash referente ao commit
2.  autor e email do usuario que fez o commit
3.  a data do commit
4.  a mensagem descritiva do commit

Porem, existem outras variacoes deste comando para logs mais objetivos.

## Opcao **--decorate**

```bash
  git log --decorate
```

Esta opcao mostra o onteudo do log normal com mais detalhes, como branchs, merges desta brach, entre outras coisas (serao abordadas mais adiante).

## Opcao **--author**

A opcao **author** vai filtar os commits feitos pelo usuario passado para esta opcao, o resultado e o que o **git log** tras, porem do autor especificado:

```bash
  git log --author="nome_do_usuario"
```

## Opcao **shortlog**

O **shortlog** vai mostrar em ordem alfabetica os seguintes items:

1. autor do commit e a quantidade realizada
2. conteudo (arquivo) do commit
3. mensagem do commit

```bash
  git shortlog
```

E uma opcao resumida de todos os commits filtrando o autor e o conteudo

### git shortlog -sn

Esta opcao tras uma forma inda mais resumida que o **shortlog**, trazendo apenas a quantidade de commits que foram realizados e o nome do autor:

```bash
  git shortlog -sn
```

## Opcao **--graph**

Esta opcao mostra de forma grafica um commit, indicando merges feitos pelo usuario em outras branchs (mais informacoes sobre a descricao dest e comando serao adicionadas mais adiante)

```bash
  git log --graph
```

## Verificando o Conteudo de um Commit pela Hash

Apos todos esses comandos para verificar o log dos commits, tambem e possivel verificar o conteudo de cada commit individualmente pela sua **hash** (aquela sequencia de caracteres grande) usitlizando a opcao **show**:

```bash
  git show 87sdfsd34sd321f654sdsdfsdf654sdfsdf48324sdf8
```

OBS: os caracteres acima no comando sao apenas um exemplo, nao representa uma **hash** real

Este comando consegue mostrar detalhes a mais do que contem ou foi adicionado no commit.
