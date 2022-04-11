# Como Criar um Alias

O git possui muitos comandos para realizar suas tarefas, e possivel abreviar ou dar um "novo nome" para um comando que voce ache longo ou cansativo, ou simplesmente para tornar mais pratico comandos que voce utiliza com frequncia.

Para fazer um alias, por exemplo, o git status pode simplesmente ser melhor utilizado sendo "git st", para adicionar esta abreviacao e necessario utilizar as configuracoes globais do git.

## Criando um alias

Abaixo segue o comando para adicionar o atalho git sh, para isso se utiliza as configuracoes globais do git (**_git config --global_**),  em seguida o alias junto a forma que se deseja utilizar (**_alias.st_**), e a funcao que vai receber o alias( **_status_**):

```bash
  git config --global alias.st status
```

Outro exemplo pode ser atribuindo um nome alias para o diff, como se trada de mostrar modificacoes, um nome mais claro poderia ser "changes", pode parecer contraproducente, mas traz mais clareza:

```bash
  git config --global alias.changes diff
```

Se voce e um iniciante no estudo do git, e interessante voce utilizar os comandos padroes para obter familiaridade com o sistema.

OBS: Estes exemplos acima sao apenas para mostrar como se comporta a funcionalidade, os exemplos nao remetem boa pratica, apenas descrevem formas de aplicacao.
