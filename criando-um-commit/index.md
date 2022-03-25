# Criando um Commit

Para criar um commit é necessário primeiro, adicionar o codigo no qual voce trabalhou para um "pacote" que ficara em aberto. Existem varias formas de se adicionar conteúdo a este pacote. Os comandos inicias são para adicionar todos os arquivos ou modificações feitas no momento:

```bash
  git add .
  git add --all
```

Para adicionar um arquivo especifico dentro do diretorio em que você está:

```bash
  git add <nome-do-arquivo>
```

Se o diretorio é outro, por exemplo, se você esta no diretorio raiz e o arquivo que você quer adicionar esta dentro da estrutura a seguir
src
|--teste
|-index.md

Acima esta a pasta src, dentro dela a pasta teste com o arquivo md (o arquivo que será adicionado ao "pacote"), o comando deve ser semelhante a este:

```bash
  git add src/teste/index.md
```
