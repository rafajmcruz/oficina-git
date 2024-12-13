
### Criando conta no Github:

Acesse o site oficial do GitHub e clique em Sign Up (Cadastrar-se). Siga as instruções!

### Instalação do Git:

#### Para Windows:

Recomendado instalar Github Desktop, que contem uma implementação do Git para terminal de comando. 

#### Para Linux:

Disponível apenas CLI (interfaces de terminal de comando)
Git CLI - 
GitHub CLI - 

#### Extensões do Git para as IDEs

Há extensões ou plugins do Github disponíveis para diversas IDEs, como VSCode, IntelliJ, PyCharm, etc. 
Para instalar, busque por Github na seção de instalação de plugins

### Autenticação no GitHub

A forma mais segura é fazer a autenticação via web browser. 
Não esqueça de realizar logout antes de sair do computador compartilhado. 

Autenticação via CLI: 

```bash
# No terminal de comando e com o programa gh instalado, digite:
gh auth login
# Selecione autenticação via navegador
# Copie o código verificador
# Siga as instruções para autenticação
```

Autenticação via Github Desktop: seguir instruções no programa


### Criando o repositório remoto

É possível iniciar um repositório vazio no github para iniciar um novo projeto ou copiar um repositório existente. 

O processo de copiar um repostório que já existe se chama `fork` 

#### Novo repositório:

No GitHub, vá para sua página de perfil e clique em Repositories.

Clique em New (Novo) e siga as instruções.

Após criar o repositório, você verá o URL para cloná-lo.

#### Fork:

Se você quiser contribuir em um repositório de outra pessoa, acesse o repositório desejado e clique no botão Fork no canto superior direito.

O repositório será copiado para a sua conta, e você poderá cloná-lo para a sua máquina local e contribuir.

### Clonando o repositório nas máquinas locais

Para copiar um repositório existente para uma máquina local, usamos o `git clone`

No GitHub, no repositório que você deseja clonar, clique em Code e copie o URL.

No terminal, vá até o diretório onde deseja armazenar o projeto e execute:

`git clone https://github.com/usuario/repo.git`

Isso criará uma cópia do repositório no seu computador.


### Fazendo alterações no projeto

Para cada grupo de alterações que você for fazer, crie uma branch diferente. 

Uma branch é um ramo do projeto no qual é mais seguro fazer alterações quando se trabalha em equipes. O ideal é que cada programador trabalhe em sua própria branch. 

Para criar uma branch, use: 

```bash
# Cria a branch
git branch <nome_da_branch>

# Altera para a branch
git checkout branch
```

Com o git setado para estar na sua própria branch, abra o projeto na IDE e faça pequenas alterações. 

### Commitando as alterações

Toda vez que um conjunto de alterações está completo, vamos avisar o Git para tirar um 'snapshot' do estado do nosso projeto até então. É como se fosse uma imagem de como está o nosso código. 

Com isto, conseguimos ter um controle das mudanças no nosso código ao longo do tempo e reverter alterações, se necessário. 

Com o git, só é possível reverter entre um snapshot e outro (o que já é suficiente para as necessidades de desenvolvimento de software).

#### O fluxo do commit

Para salvar uma versão do nosso código, seguimos a sequência de ações:

```bash
git status

git add <nome_do_arquivoA> <nome_do_arquivoB> 
# ou git add .  

git commit -m "Mensagem de commit personalizada"
```

**git status** - Antes de fazer um commit, verifique quais arquivos foram alterados com:

**git add .** - Para adicionar todos os arquivos modificados

**git add nome-do-arquivo** - Para adicionar um arquivo específico

**git commit -m "Mensagem do commit"** - Depois de adicionar os arquivos, faça o commit com uma mensagem explicativa



### Atualizar o repositório remoto

Para enviar suas alterações para o repositório remoto no GitHub:

`git push origin nome-do-branch`

Nota: O origin é o nome do repositório remoto, e nome-do-branch é o branch em que você está trabalhando (geralmente main ou master).

### Mesclar a sua branch com um Pull Request no Github:

#### Na página do seu repositório no github:

Escolha a branch de origem (nome_do_branch)

Escolha a branch de destino (geralmente main ou develop).

Adicione um título e descrição para explicar o que foi feito.

#### Revise, ajuste e resolva conflitos, se necessário:

Outros desenvolvedores revisam o código.

Se solicitado, ajuste o código na branch de origem e envie novamente:

`git push origin nome_da_branch`

#### Mescle o Pull Request:

Após aprovação, clique em "Merge" no GitHub.


### Resolver conflitos de merge

Situação de conflito: Quando dois colaboradores alteram a mesma parte de um arquivo, um conflito pode ocorrer ao tentar fazer o merge.

Quando um conflito de merge acontecer, o Git vai marcar os arquivos com conflitos.

Abra o arquivo em conflito e procure as marcações:

> <<<<<<< HEAD
> 
> (seu código)
>
> =======
>
> (código do outro colaborador)
>
> ->>>>>>> nome-do-branch

Edite o arquivo para resolver o conflito, mantendo ou combinando as alterações.
Após resolver, adicione o arquivo ao stage:

`git add nome-do-arquivo`

Complete o merge com:

`git commit`

Finalizar o merge: Depois de resolver todos os conflitos, faça o commit final e envie as alterações para o repositório remoto:

`git push origin nome-do-branch`



### Baixar atualizações do repositório para a máquina

É muito importante manter o seu código local atualizado com as alterações enviadas por você ou outros colabores ao repositório online. Para atualizar seu código local com o remoto, use: 

`git pull`
