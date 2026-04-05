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

git init    No seu ambiente local, inicialize o Git na pasta do projeto. Conecte o repositório remoto usando git remote add origin URL-do-repositorio-GitHub.
git remote add origin URL-do-repositorio-GitHub     Conectando o repostirorio local ao remoto 

2.3 Configuração de usuário (primeiro uso)

Se for a primeira vez usando Git, configure o usuário com git config --global user.name "Seu Nome" e git config --global user.email "seu@email.com".

2.4 Clonando repositório existente

Se o repositório já existia e você ainda não tem nada na sua pasta local, pode cloná-lo usando git clone URL-do-repositorio.
Se na sua pasta local ja existem coisas, pode se usar git pull para trazer as mudancas do remoto para o local 

2.5 Arquivos essenciais

Crie um arquivo README.md com a descrição e instruções do projeto. Crie um arquivo .gitignore para marcar arquivos que não serão enviados para o repositório remoto por questões de segurança, como .env e .venv. O arquivo .env deve armazenar dados sensíveis, como senhas, logins e chaves de API, e sempre deve ser ignorado pelo .gitignore.

2.6 Processo de versionamento

Para salvar mudanças e enviá-las ao remoto:

Adicione arquivos ao stage usando git add ., o ponto final adiciona todos os arquivos do projeto, exceto os ignorados pelo .gitignore.
git commit -m "nome-commit"      (Salve as mudanças localmente.)
git push origin nome-branch (Envie as mudanças para o repositório remoto.)

Esse é o fluxo básico do dia a dia para versionar projetos.

2.7 Atualizando repositório local

Para trazer alterações do repositório remoto para sua máquina, use git pull origin main.

2.8 Git Fetch

O comando git fetch é usado para baixar atualizações do repositório remoto sem aplicá-las imediatamente na sua branch atual.

Ele atualiza referências locais de todas as branches remotas (como origin/main), mas não altera o conteúdo da sua branch atual.
É útil quando você quer ver quais alterações foram feitas remotamente antes de decidir fazer merge ou rebase.
Após um git fetch, você pode comparar sua branch atual com a versão remota, e só então integrar mudanças manualmente usando git merge ou git rebase.
Em resumo: git fetch = “trazer informações do remoto sem misturar nada no que estou trabalhando agora”.
2.9 Branchs

Branchs são ramificações do fluxo principal do código. Elas permitem trabalhar em funcionalidades separadas sem impactar o código principal. Por exemplo, a branch main pode conter a versão original do projeto, enquanto uma branch feature é usada para testar novas funcionalidades. Alterações só aparecem na main após um merge.

Comandos básicos de branch:
Criar branch: git branch nome-branch
Trocar de branch: git switch nome-branch
Criar e trocar de branch ao mesmo tempo: git checkout -b nome-branch
2.10 Merge (junção de branchs)

O merge permite juntar alterações de uma branch em outra. Pode ser feito pelo GitHub (forma visual) ou pelo terminal. O merge sempre acontece na branch que está ativa, juntando nela as alterações da branch selecionada. Por exemplo, para juntar a branch feature/login na main, você deve primeiro estar na main e depois fazer o merge da feature/login.

3️⃣ Quickstart
3.1 Fluxo básico

Criar repositório → conectar ao GitHub → adicionar arquivos → commit → push.

3.2 Fluxo de atualização

Pull → editar código → add → commit → push.

3.3 Fluxo com branch

Criar branch → desenvolver funcionalidades → merge → enviar para o remoto.

4️⃣  Estrutura de um Repositório GitHub Profissional

Um repositório profissional deve ser organizado, seguro e fácil de entender. Ele precisa deixar claro o que o projeto faz, como usar e garantir que informações sensíveis não sejam expostas.

4.1 Arquivos essenciais
README.md
Documento principal do projeto. Deve conter descrição, instruções e contexto do que está sendo desenvolvido.
.gitignore
Arquivo responsável por definir o que não será enviado ao repositório remoto, evitando arquivos desnecessários ou sensíveis.
.env
Arquivo onde ficam armazenadas informações confidenciais, como senhas, logins e API keys. Deve sempre ser ignorado pelo .gitignore.

requirements.txt
arquivo onde ficam todas as dependencias (como bibliotecas) do seu codigo,importante para que seu codigo possa ser reutilizado em outras maquinas.
Arquivo precisa ficar de preferencia na raiz do projeto
possivel criar automaticamente um arquivo requirementes usando pip freeze > requirements.txt

4.2 Organização básica
Separar arquivos do projeto de forma clara
Evitar misturar código com arquivos desnecessários
Manter uma estrutura simples e compreensível

4.3 Boas práticas
Nunca enviar dados sensíveis para o GitHub
Sempre utilizar .gitignore corretamente
Manter o README atualizado e explicativo
Garantir que o projeto seja fácil de entender por outras pessoas



5️⃣4️ Comandos extras úteis
git status → Ver o status do repositório.
git log → Ver histórico de commits.
git branch → Ver branches existentes.
git remote -v → Ver repositórios remotos.
git fetch → Baixar alterações do remoto sem aplicá-las imediatamente.
git --help --> lista alguns comandos uteis

============================================================================================================
PARTE 2 DA AULA - REVISANDO BÁSICOS DE INTRODUÇÃO À PROGRAMAÇÃO
Essa parte da aula passara brevimente pelos conceitos ja mostrados na aula do Leo para poder dar mais atencao a alguns 
assuntos importantes que nao foram mostrados. 

COLAB COM A PRATICA : https://colab.research.google.com/drive/1XJhNcn9kg6DLE9xaa1PJQFNYCHC3Vj6r?usp=sharing

------> Conceitos ja vistos: 

1 - Tipos de dados:
string = dados de texto,precisa de aspas simples ou duplas ''
int = numeros inteiros sem virgula 
float = numeros com virgula (numeros flutuantes)
bool = dados booleanos (True or False)

1.1 Comandos interessantes para strings:
De forma resumida,strings funcionam como listas,onde cada letra numa frase apresenta um index e pode ser procurado tal qual 
em uma lista.

#len = mostra o tamanho da coisa
#[0:10],[:10],[0:10:2] = mostra os indices 
#.count('exemplo') = conta qnts vezes um caracter/caracteres apareceu
#.find('exemplo') = acha a posicao em q determinado caracter/s esta
#.upper() = tudo maiusculo
#.lower() = tudo minusculo
#.capitalize() = deixa a primeira letra da string em maiusculo
#.title() = deixa o inicio de cada palavra em maiusculo,bom usar .strip antes
#.strip() = tira espacos inuteis
#.split()=separa as palavras de uma frase com base nos espacos,transformando em uma lista
#'exemplo'.join() = separa as palavras com oq esta entre aspas, bom usar split antes se nao separa letra por letra
#exemplo.lower().find('exemplo') = minuscula tudo e caça determinado trecho


2 - Estruturas de condicao :
O codigo segue diferentes caminhos com base em condicoes (funciona a base da logica matematica)

if x == x:
    print("x é igual a x")
elif x == y:
    print(x é igual a y)
else:
    print(x nao é igual a nada)

2.1 Outros exemplos de if:
if not x:
if x and y:
if x or y:

2.2 Diferenca entre usar varios If e usar Elif:
Ao usar varios If,o codigo ira analisar todas as condicoes,ou seja,mesmo que uma condicao if anterior for verdadeira,
todas as outras serao checadas,possibilitando que varias condicoes sejam executadas.
- Com Elif,assim que uma condicao for cumprida,as outras deixam de ser analisadas. Cenario bom para quando so queremos uma 
condicao sendo executadas,ao inves de multiplas. 

3 - Lacos de Repeticao: 
For = Usado quando você sabe quantas vezes quer repetir ou quer iterar sobre uma coleção (lista, tupla, string, etc.).

- Sintaxe básica:
for i in range(5):  # repete 5 vezes: 0,1,2,3,4
    print(i)

ou percorrendo listas

frutas = ["maçã", "banana", "laranja"]
for fruta in frutas:
    print(fruta)

While = Usado quando você não sabe quantas vezes vai repetir, mas quer repetir enquanto uma condição for verdadeira.

Sintaxe básica:
contador = 0
while contador < 5:
    print(contador)
    contador += 1


4 - Definindo funcoes : 
Funcoes sao blocos de codigo reutilaveis. A estrutura delas é feita de def nome_funcao(parametros):
onde os parametros sao informacoes que serao utilizadas dentro da funcao
ex:
def saudacao(nome):
    print(f"{nome}")

chamando a funcao
saudacao(nome)

4.1 Funcoes tambem podem retornar valores
def soma(a,b):
    a+b

resultado = soma(4,3)
print(resultado)


--- Coneceitos nao Vistos:

1. Estruturas de dados compostos

Estruturas de dados compostos permitem armazenar múltiplos valores e organizar informações complexas.

Listas

Coleções ordenadas e mutáveis.
Métodos importantes:
append(valor) → adiciona no final da lista.
insert(indice, valor) → insere valor em posição específica.
remove(valor) → remove a primeira ocorrência do valor.
pop() → remove o último elemento (ou o da posição indicada).
sort() → ordena a lista.
len(lista) → retorna tamanho da lista.
Exemplo em texto: lista frutas = ["maçã", "banana", "laranja"]; adicionar "pera" → frutas.append("pera"); remover "banana" → frutas.remove("banana").

Tuplas

Coleções ordenadas e imutáveis.
Úteis para valores fixos ou constantes, como coordenadas ou configurações que não devem mudar.
Métodos importantes:
len(tupla) → retorna tamanho da tupla.
count(valor) → conta quantas vezes o valor aparece.
index(valor) → retorna a posição da primeira ocorrência do valor.
Exemplo em texto: tupla coordenadas = (10, 20); acessar coordenadas[0] → 10; contar quantas vezes 20 aparece → coordenadas.count(20) → 1.

Dicionários

Coleções de pares chave-valor, úteis para associar dados de forma estruturada.
Métodos importantes:
dicionario.keys() → retorna todas as chaves.
dicionario.values() → retorna todos os valores.
dicionario.items() → retorna pares chave-valor.
dicionario.get(chave) → retorna valor associado à chave, sem gerar erro se não existir.
dicionario.update({"chave": valor}) → adiciona ou atualiza valor.
Exemplo em texto: usuario = {"nome": "Ana", "idade": 25, "email": "ana@email.com"}; acessar usuario["nome"] → "Ana"; atualizar idade com usuario["idade"] = 26; obter todas as chaves → usuario.keys() → ["nome", "idade", "email"].

Boas práticas:

Usar listas para coleções mutáveis, tuplas para valores fixos e dicionários para dados associados.
Iterar de forma clara e evitar alterações inesperadas de dados importantes.




2. Tratamento de erros (try e except)

Permite que o programa continue executando mesmo quando um erro ocorre.
try → bloco onde o código que pode gerar erro é executado.
except → bloco que define o que fazer caso um erro ocorra.
else → bloco que so roda caso nao tenham erros captadaos pelo except
finally → bloco que sempre roda,indepentende dos erros

É possível capturar tipos específicos de erro para maior controle.

Exemplo em texto:

Tentar dividir dois números; se o divisor for zero, exibir "Erro: divisão por zero" sem interromper o programa.
Tentar abrir arquivo que pode não existir; se ocorrer FileNotFoundError, exibir mensagem de alerta.

Boas práticas:

Tratar apenas erros esperados, evitando capturar exceções genéricas desnecessariamente.
Fornecer mensagens úteis para usuário ou registrar logs para depuração.





3. Modularização

Organizar o código em módulos (arquivos separados) com funções e classes específicas.
Permite dividir responsabilidades, facilitar manutenção e reutilizar código.
Um módulo pode ser importado em outro, permitindo aproveitar funções e classes já definidas.

Módulos que você quer importar precisam estar na mesma pasta do script principal ou em subpastas com __init__.py (para pacotes).
Se estiver em subpasta sem __init__.py, o Python pode não reconhecer como pacote. No vscode com python,ao tentar importar modulos,é criado automaticamente
um arquivo __pychache__ com as informacoes necessarias pra ser possivel importar coisas daquela pasta

Exemplo em texto:

Criar módulo funcoes_matematica.py com função soma(a, b) → importar no arquivo principal e usar soma(4, 3).
Separar funções de visualização, processamento de dados e lógica de negócio em módulos distintos.

Exemplo:
meu_projeto/
│
├─ main.py            # Arquivo principal
├─ funcoes_matematica.py  # Módulo com funções
└─ utils/
    ├─ __init__.py    # Torna a pasta um pacote
    └─ funcoes_gerais.py     # Outro módulo

from funcoes_matematica import soma, divisao, multiplicacao

Boas práticas:

Manter cada módulo focado em um propósito específico.
Evitar duplicação de código.
Documentar funções e módulos com comentários claros.



