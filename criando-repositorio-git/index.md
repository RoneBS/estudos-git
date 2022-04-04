# Criando um Repositorio _**Git**_

Para criar um repositorio **git**, basta utilizar o comando "git init" no diretorio onde o projeto ficara alocado:

```bash
git init
```

## Linkando Seu Repositorio Local para o Github

Apos criar o seu repositorio, voce ja pode fzer o link do seu repositorio local para o github, e necessario adicionar algum conteudo no repositorio, como o README.md por exemplo, em seguida fazer o commit, ha a opcao de renomear a branch de **_master_** para **_main_**. Agora e necessario copiar o endereco do repositorio criado no github (o repositorio remoto no github precisa estar criado para esta acao ser realizada), por fim, fazer o **_push_** para o repositorio remoto e definilo como padrao:

```bash
  git add README.md
  git commit -m "first commit"
  git branch -M main
  git remote add origin https://github.com/seu-usurario/nome-do-projeto.git
  git push -u origin main
```

Descrevendo melhor o que estes comandos fazem, o **_commit -m_** faz a acao de fechar o pacote do conteudo que esta em **_stage_**, a opcao -m da a opcao de adicionar uma mensagem ao commit.

O comando **_git branch -M main_** esta renomeando a branch que tem como padrao o nome **_master_** para **_main_**, a opcao -M e indicada caso deseja mudar a capitalizacao de uma letra (mudar para maiuscula ou minuscula), pois ela muda o nome de uma branch mesmo que ela ja exista, mas se recomenda utilizar **_git branch -m_** para fazer a alteracao para um novo nome.

OBS: Repare que a opcao -m tem um efeito diferente para fazer um commit ou renomear uma branch.

O comando **_git remote add origin_** vai indicar o endereco passado como o repositorio remoto, sera para ele que o conteudo do repositorio local sera enviado.

Por fim, **_git push -u origin main_**, aqui nos temos varias coisas acontecendo, o push esta fazendo o envio dos commits realizados para o repositorio remoto, a opcao -u e uma abreviacao do depreciado -set-upstream, que define o branch remoto como padrao para o branch local atual (no caso o main), o origin indica o nome dado a este repositorio remoto, poderia ser utilizado qualquer outro nome, mas por padrao este e o nome adotado, e main e justamente a branch que e indicada como local para origin.
