Encontro 1 - Git e GitHub na Prática + Revisão de Básicos
README do Apresentador

Este documento organiza a apresentação da aula e serve como guia conceitual para o expositor. A estrutura abaixo deve ser seguida para garantir clareza, progressão lógica e alinhamento com o grupo.

1️⃣ Motivação
1.1 Uso profissional do Git e GitHub

Versionar código é essencial para salvar, organizar e compartilhar projetos. O GitHub permite armazenar repositórios remotos e colaborar com outras pessoas.

1.2 Contexto da aula

Continuação das aulas de introdução à programação. Aplicação prática de Git e GitHub no desenvolvimento de projetos.

2️⃣ Como Funciona
2.1 Criando repositório no GitHub

Crie um repositório no GitHub. Configure para criar o repositório sem README, .gitignore e licença inicialmente.

2.2 Conectando Git local ao GitHub

No seu ambiente local, inicialize o Git na pasta do projeto com git init. Conecte o repositório remoto usando git remote add origin URL-do-repositorio-GitHub.

2.3 Configuração de usuário (primeiro uso)

Se for a primeira vez usando Git, configure o usuário com git config --global user.name "Seu Nome" e git config --global user.email "seu@email.com".

2.4 Clonando repositório existente

Se o repositório já existia e você ainda não tem nada na sua pasta local, pode cloná-lo usando git clone URL-do-repositorio.

2.5 Arquivos essenciais

Crie um arquivo README.md com a descrição e instruções do projeto. Crie um arquivo .gitignore para marcar arquivos que não serão enviados para o repositório remoto por questões de segurança, como .env e .venv. O arquivo .env deve armazenar dados sensíveis, como senhas, logins e chaves de API, e sempre deve ser ignorado pelo .gitignore.

2.6 Processo de versionamento

Para salvar mudanças e enviá-las ao remoto:

Use git add . para adicionar todos os arquivos modificados ao stage, exceto os ignorados pelo .gitignore.
Use git commit -m "nome_commit" para salvar as mudanças localmente.
Use git push origin main para enviar as mudanças salvas para o repositório remoto.

Esse é o fluxo básico do dia a dia para versionar projetos.

2.7 Atualizando repositório local

Para trazer alterações do repositório remoto para sua máquina, use git pull origin main.

2.8 Branchs

Branchs são ramificações do fluxo principal do código. Elas permitem trabalhar em funcionalidades separadas sem impactar o código principal. Por exemplo, a branch main pode conter a versão original do projeto, enquanto uma branch feature é usada para testar novas funcionalidades. Alterações só aparecem na main após um merge.

Comandos básicos de branch:
Criar branch: git branch nome-branch
Trocar de branch: git switch nome-branch
Criar e trocar de branch ao mesmo tempo: git checkout -b nome-branch
2.9 Merge (junção de branchs)

O merge permite juntar alterações de uma branch em outra. Pode ser feito pelo GitHub (forma visual) ou pelo terminal. O merge sempre acontece na branch que está ativa, juntando nela as alterações da branch selecionada. Por exemplo, para juntar a branch feature/login na main, você deve primeiro estar na main e depois fazer o merge da feature/login.

3️⃣ Quickstart
3.1 Fluxo básico

Criar repositório → conectar ao GitHub → adicionar arquivos → commit → push.

3.2 Fluxo de atualização

Pull → editar código → add → commit → push.

3.3 Fluxo com branch

Criar branch → desenvolver funcionalidades → merge → enviar para o remoto.

4️⃣ Comandos extras úteis
git status → Ver o status do repositório.
git log → Ver histórico de commits.
git branch → Ver branches existentes.
git remote -v → Ver repositórios remotos.
git fetch → Baixar alterações do remoto sem aplicá-las imediatamente.