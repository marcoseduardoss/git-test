# Principais comandos e testes Git - V-2.0.0

Fluxo de trabalho:
---
Seus repositórios locais consistem em três "árvores" mantidas pelo git. a primeira delas é sua Working Directory que contém os arquivos vigentes. a segunda Index que funciona como uma área temporária e finalmente a HEAD que aponta para o último commit (confirmação) que você fez.

Você pode propor mudanças (adicioná-las ao Index) usando ("git add <arquivo>" ou "git add *". Este é o primeiro passo no fluxo de trabalho básico do git. Para realmente confirmar estas mudanças (isto é, fazer um commit), use 'git commit -m "comentários das alterações"' Agora o arquivo é enviado para o HEAD, mas ainda não para o repositório remoto.

  #### Se você não clonou um repositório existente e quer conectar seu repositório a um servidor remoto, você deve adicioná-lo com
###### $ git remote add origin git@github.com:git/git.git
Obs.: O "origin" não é o nome do repositório remoto. É um alias local definido como uma chave no lugar da URL do repositório remoto. O uso do alias, evita que o usuário digite toda a URL remota ao solicitar um push. Por convenção, o repositório remoto padrão é chamado "origem", mas você pode trabalhar com vários controles remotos (com nomes diferentes) ao mesmo tempo. 
  
  #### Renomear alias definido como uma chave no lugar da URL do repositório remoto
###### $ git remote rename origin mynewalias

  #### Enviar alterações ao seu repositório remoto (poderia ser outra branch qualquer, ex.: branch-qualquer):
###### $ git push git@github.com:git/git.git master
ou
###### $ git push origin master
ou
###### $ git push origin branch-qualquer
 
  #### Criar e Trocar de branch de uma vez só:
###### $ git checkout -b new-branch
Nota: "git checkout -b new-branch" é o atalho de "git branch new-branch" seguido por "git checkout new-branch".
  
Links úteis:
--
1. https://githowto.com/pt-BR/navigating_branches  
https://rogerdudler.github.io/git-guide/index.pt_BR.html