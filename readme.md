Passos para usar o git/github

1 baixe e instale o git 
(https://git-scm.com/downloads)

2 configure o git pelo terminal 
git config --global user.name "username"
git config --global user.email "useremail"

3 Crie a pasta do seu projeto abra o terminal acesse ela e rode o comando a seguir
git.init

4 Crei seu repositorio no github

5 Gerando a chave SSH
*abra o terminal e rode o comando (ssh-keygen -t rsa -b 4096 -C "SeuEmail@exemplo.com") 
*apos rodar isso de 3 enter

6 Pegando a chave SSH
*depois de gerar a chave entre na pasta ssh pelo terminal usando (cd ~/.ssh)
*apos entrar no diretorio ssh rode o comando (cat id_rsa.pub) isso vai mostrar a sua chave

7 Adicionando a chave no git
Apos gerar a sua chave copie ela entre no git hub busque a parte de segurança SSH keys
*New SSH Key - de um nome para ela exemplo casa / trabalho e cole a chave copiada 

8 Conectando repositoriolocal com o remoto
*abra seu projeto criado no git ele vai te dar a instrução do comando que deve rodar no repositorio local para conectalo no meu caso foi 
(git remote add origin https://github.com/@SeuEsuarioGit/@SeuProjeto.git)

----------------------------------

comandos basicos
 Git add * adiciona suas mudanças para comitar
 Git commit -m 'msg'* usado para escrever as alterações feitas nessa versão
 Git push * usado para subir seu codigo local para o remoto
 Git pull * usado para atualizar o codigo local com mudanças do remoto

 font ( https://www.freecodecamp.org/portuguese/news/10-comandos-do-git-que-todo-desenvolvedor-deveria-conhecer/ )


 ---------------------------- 
 branch 

 serve para que multiplas pessoas possam trabalhar ao mesmo tempo sem a necessidade de alterar a master 
 exemplo da pra usar pra ajustar um bug enquanto outras pessoas continuam trabalhando no projeto 

*para criar um branch basta rodar o comando
    git checkout -b nome_do_branch

*para mudar entre os branch basta digitar
    git checkout nome_do_branch

*para deletar um branch basta digitar
    git branch -D nome_do_branch

---------------------------
Merge

De forma resumida o Merge serve para unir branch mantendo o historico mais criando um novo comit que de certa forma e desnecessario
c1-c2----c5-----c6  
     \--c3-c4-/
(os c sao comites c1,c2 e c5 sao do master  c3 e c4 sao de uma ramificação usando o marge unimos ambos com um novo comir o c6)

Rebase

Diferende do Marge que cria um comit novo o Rebase pega as mudanças do Branch e coloca no inicio da fila ou seja ele pega td aquilo que foi feito em outro Branch e comita como se fosse um novo comite linear mantendo assim uma unica ramificação, entretanto perdese o historico cronologico e pode gerar problemas caso mais de uma pessoa esteja trabalhando no mesmo 'arquivo' que foi midificado com o Rebase
