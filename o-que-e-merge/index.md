# O que e **Merge**?

O **_merge_** e o metodo que mescla (une) as modificacoes entre dois branchs. Um projeto que possui varias pessoas trabalhando, frequente desenvolvimento de novas funcoes, controle das versoes, correcoes entre outras atividades, certamente divide todo este fluxo com branchs, sendo que o branch principal recebe apenas o conteudo final, e para isso e necessario trazer desses outros branchs o conteudo trabalhado, e e ai que entra o **_merge_**, fazendo a mescla do conteudo de um branch de uma release ou qualquer outra atividade, para o branch main.
Quando o **_merge_** e realizado, ele cria um novo commit indicando a juncao do conteudo dos respectivos branchs mesclados.

Isso e importante para que determinadas atividades sejam feitas isoladas do branch principal, para melhor controle, clareza no tratamento do codigo, seguranca entre outras vantagens.

O comando para fazer o **_merge_** e simples, basta estar no branch que voce deseja receber o conteudo do branch que se deseja mesclar, um exemplo simples e:
Se voce fez uma nova feature (que esta no branch "features") e quer adicionar este conteudo ao branch main, faca o **_checkout_** para o branch main e o comando a seguir:

```bash
  git merge features
```
