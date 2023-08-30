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

