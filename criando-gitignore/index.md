# Criando o **.gitignore**

Nos repositorios dos projetos alguns arquivos nao necessitam ir ao repositorio remoto, ou nao devem, sejam arquivos desnecessarios ou keys que nao devem estar expostas. Para isso existe o arquivo **_.gitignore_**, ele serve para que esses arquivos que nao devem ser enviados ao repositorio remoto sejam listados e ignorados pelo tracker do git, ficando invisiveis e inrastreaveis, desta forma nao podem ser enviados em um commit ao repositorio remoto.

Para fazer um arquivo .**_gitignore_**, basta criar um arquivo na raiz do projeto com este nome, dentro deste arquivo as regras vao ser adicionadas para cada tipo de arquivo.

Um site que ajuda muito a criar os arquivos de acordo com tecnologia e o <https://www.toptal.com/developers/gitignore>, voce pode adicionar as tecnologias que esta trabalhando no projeto e criar um gitignore destas tecnologias, fica somente uma ressalva para utilizar somente o que for necessario, pois faz uma lista vasta de coisas que talvez nao precisem ser ignoradas.

Abaixo segue um exemplo utilizando o site e o resultado q ele gera para um projeto utilizando React:

```bash
  ### react ###
  .DS_*
  *.log
  logs
  **/*.backup.*
  **/*.back.*

  node_modules
  bower_components

  *.sublime*

  psd
  thumb
  sketch
```
