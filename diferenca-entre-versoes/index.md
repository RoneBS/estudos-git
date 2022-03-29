# Verificando Diferenca entre Versoes

Depois de usar o **_git log_** para ver as adicoes feitas no repositorio , agora sera utilizado um novo comando para verificar o que foi alterado:

## Opacao **diff**

O **_git diff_** vai mostrar as alteracoes feitas por ultimo no cache do pacote antes de fecha-lo para ser comitado

```bash
git diff
```

OBS: sempre e valido utilizar o **_git diff_** antes de fazer um commit, para verificar o estado do cache do pacote antes de fazer o commit, isso ajuda a previnir erros ou alteracoes que nao deviam ser enviadas no commit

## Opcao **--name-only**

O **_git diff_** possui uma opcao para mostrar somente o nome do arquivo editado, se voce possui uma lista grande de arquivos alterados, essa e uma boa opcao para deixar o terminar mais legivel e objetivo

```bash
git diff --name-only
```
