# Resumos Git e GitHub

Repositório para armazenar resumos sobre Git e Github do curso de versionamento de código com o Git e Github da [Digital Innovation One](https://www.dio.me)

## Documentação Git📚
- [Documentação Git](https://git-scm.com/docs/git/pt_BR)
- [Documentação Github](https://docs.github.com/pt)
## Sumário 📓
| Índice | Resumos|
|-------| --------|
| 1°⚙| Configurações do Git|
| 2° 🔰| Criando e Clonando Repositórios|
|3°📩|Salvando Alterações no Repositório Local|
|4°📤| Enviando e Baixando Alterações com o Repositório Remoto|
|5° ❌|Desfazendo Alterações no Repositório Local|
|6°🔑|  Trabalhando com Branches|
|7°👩‍💻|  Comandos Úteis no Dia a Dia para Branches|

## Configurações Git ⚙ 

Informações da Ferramenta
```
Informações da Ferramenta

git config
``` 
Configurar Email e Nome Global
```
git config --global user.name "coloque seu nome"

git config --global user.email "coloque seu email"

```
Colocando a Branch em main
```
git config init.defaultBranch

git config --global init.defaultBranch main

```
Listando os caminhos da variáveis

```
git config --global --list
```
## Criando e Clonando Repositório 🔰
Criando um diretório e entrando nele
```
mkdir (nome do seu diretório)

cd (nome do seu diretório)
```
Transformando em um repositório git
```
git init

cd .git
```
Configurações do diretório
```
cat config
```
Clonando o Repositório no GitHub em https
```
git clone (nome da url do repositório) Mudança de nome (opcional)
```
Criando Git remotos
```
cd /caminho/para/sua/pasta
git init
git remote add origin https://github.com/usuario/nome-do-repositorio.git
git add .
git commit -m "Primeiro commit"


```
Vendo o que tem dentro do repositório
```
git log
```
Repositório que tem váriais Branch
```
git clone URL --branch feature-1 --single branch
```
## Salvando Alterações no Repositórios locais 📩
Monstrando a area de trabalho
```
git status #Mostrar os commits e estados dos arquivos
```
Criando um README.md
```
touch README.md
```
Abrindo no editor
```
code .
```
Adicionando no git
```
git add README.md 
```
Criando um Commit
```
git commit -m"(nome do commit)"
```
Git Ignore: para não salvar no commit
```
echo (nome do diretório) > .gitignore #colocar o git Ignore
echo > .gitignore #tirar o git Ignore
```
Git Keep: para dizer que há um diretório vazio
```
touch (nome do arquivo) .gitkeep
```
## Enviando e Baixando Alterações com o repositório remoto 📤
Conectando no repositorio remoto
```
git remote add origin (A URL)
```
Enviando as Alterações
```
git push -u origin main
```
Recebendo as Alterações
```
git pull origin (nome-da-branch)

```
## Desfazendo Alterações no Repositório Local ❌
Remover todos os arquivos
```
rm -rf .git
```
Para restaurar o arquivo apagado
```
git restoure (nome do arquivo)
```
Renomeando Commit
```
git commit --amend -m"(nome novo)"

#outro jeito:

git commit --amend
#Pressione Esc para garantir que você está no modo de comando.
#Digite :wq e pressione Enter. Isso salva as alterações e sai do editor.

```
Desfazendo um Commit
```
#Desfazendo arquivo
git reset (nome do arquivo)

git restoure --staged (diretório)

git reset --soft (ID do commit)

git reset --mixed (Id do commit ) ou git reset 

git reset --hard (ID do commit)

```
Diferença:
| Modo | HEAD movido | Área de standing(index) | Diretório de Trabalho |
| ------ | ---------- | -----------------------| ----------------------|
| '--soft' | Sim | Não | Não |
| '--mixed' | Sim | Sim | Não |
| '--hard' | Sim | Sim | Sim |

Histórico dos commit
```
git reflog
```
## Trabalhando com Branches 🔑

Criando uma Branch
```
git checkout -b (nome da nova branch)
```
Mudando uma Branch
```
git checkout (nome da branch)
```
Para ver os ultimos commit das branch
```
git branch -v
```
Delentando Branch
```
git branch -d (nome da branch)
```
Conflitos de Branch: caso um commit seja alterado la no github ou outra pessoa tenha mudado ele e você não tenha essas alterações em sua máquina, faça os seguintes passos:

Pegue o arquivo editado pela outra pessoa
```
git pull
```

Depois faça a sua alteração e envie de novo 
```
git push origin main
```

## Comandos Úteis no Dia a Dia com Branches 👩‍💻
Para resolver o problema anterior com mais facilidade utilize:
```
git origin main
```
Para ver das branch locais e remotas
```
git diff main origin/main

#agora para pegar essas alterações depois do git diff

git marge (nome do repositorio)
```