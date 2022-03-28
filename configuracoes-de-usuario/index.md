# Configuracoes de Usuario

Para configurar suas informacoes no git e usado a flag **--global**. Com ela voce pode passar o nome do seu usuario, email, configurar o editor e varias outras opcoes.

Aqui nos veremos configuracoes basicas, a de nome de usuario, email e configuracao do editor padrao do git no terminal.
OBS: O git por padrao usa o vim como editor.

## Configurando Nome de Usuario

```bash
  git config --global user.name "nome_do_seu_usuario"
```

## Configurando Email de Usuario

```bash
  git config --global user.email "email_do_seu_usuario"
```

## Configurando o Editor Padrao do Git

```bash
  git config --global core.editor "nome_do_editor"
```

Voce pode verificar as informacoes utilizando os mesmos comandos sem a flag **--global**:

```bash
  git config user.name
```
