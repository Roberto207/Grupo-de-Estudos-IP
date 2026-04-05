Encontro 1- Git e github  na pratica e  Revisando Básicos (levando em consideracao as aulas de IP do Leo)

# 1 - REPOSITORIO NO GITHUB PROFISSIONAL ALINHADO COM GIT LOCAL:
1- Passo = Crie um repositório no Github

1.1 - Nas configuracoes de criacao,selecione pra criar o repositorio sem arquivo README ou .GITIGNORE (e sem licenca por enquanto). Crie o repositório.

1.2 - No seu ambiente de desenvolvimento,inicie o git na sua pasta e depois a conecte ao seu repositório remoto.
-git init
-git add remote origin url-repositório-github             (ex:https://github.com/seu-usuario/Repositorio-exemplo.git)

1.3 - Se for a primeria vez usando git,ele pode pedir pra configurar o seu usuario do github
git config --global user.name "Seu Nome" 
git config --global user.email "seu@email.com"

1.4 - Se o repositório ja existia antes,possui conteudo e voce nao fez nenhuma alteracao na sua pasta local,é possivel clonar o repositorio remoto pra dentro da sua pasta
-git clone 

1.5 - Crie um arquivo README.MD com a descricao e instrucoes do seu projeto e um arquivo .gitignore que serve pra marcar arquivos que nao serao enviados para o repositorio remoto por questoes de seguranca (como o .env e o .venv)

1.6 - Arquivo .env = arquivo onde serao guardadas senhas pessoais,logins,api_keys etc. Tudo de confidencial e pessoal deve ser guardado pelo .env