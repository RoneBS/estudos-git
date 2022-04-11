# Utilizando Tags

A utilizacao de tags no git tem como uma das finalidade dar uma descricao a uma versao, release e etc.

No caso de uma release da versao 1.0.0 de um projeto, voce pode fazer uma tag descrevendo algumas coisas. E possivel passar uma anotacao com algum dado e uma mensagem, por ser uma tag annotated, este comando seria passado da seguinte forma:

```bash
  git tag -a 1.0.0 -m "Primeira versao finalizada"
```

## Enviando as Tags ao Repositorio Remoto

Depois de ter finalizado a tag, ela precisa ser enviada ao repositorio remoto, para isto basta utilizar a opcao **_--tags_**.

```bash
  git push origin main --tags
```

Neste momento, ao acesar o github, a aba release vai ser atualizada contendo um item, que sera a tag que acabou de ser enviada. Ela contem o numero passado, a mensagem descritiva, tambem estara disponivel arquivos em zip e tar.gz para download.

Para listar as tags, basta utilizar o **_git tag_**:

```bash
  git tag
```
