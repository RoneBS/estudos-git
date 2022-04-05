# Clonando um Repositorio do GitHub

Ao longo dos seus estudos com programacao, voce pode se deparar com a necessidade de baixar um repositorio remoto seu, no caso de algum problema com a sua maquina ou alguma alteracao que quebrou o projeto no seu repositorio local, assim voce pode baixar a versao estavel que esta no seu repositorio remoto. A acao a ser feita e clonar este repositorio para a sua maquina atraves do comando **_git clone_**:

```bash
  git clone https://github.com/seu-usurario/nome-do-projeto.git
```

O comando funciona ao indicar o endereco http do repositorio, ou sua chave ssh, tambem epossivel utilizando o cli do github:

```bash
  gh repo clone nome-do-usuario/nome-do-repositorio
```

Todas essas opcoes podem ser verificadas na aba **_code_** do repositorio no github.
