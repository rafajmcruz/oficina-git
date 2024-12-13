# Oficina de Git


As atividades para serem realizadas em duplas


## 1. Criar conta no Github

[www.github.com](www.github.com)

## 2. Instalação do Git:

### Para Windows:

[Instalando Git e Github](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git)

### Para Linux:

[Instalando Git](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git)

[Github CLI para Linux](https://cli.github.com/)

### Extensões do Git para as IDEs

Para instalar, busque por Github na seção de instalação de plugins

## 4. Autenticação no GitHub

A forma mais segura é fazer a autenticação via web browser. 

Não esqueça de realizar logout antes de sair do computador compartilhado. 

Autenticação via Github Desktop: siga as instruções no programa

Autenticação via CLI: 

```bash
# No terminal de comando e com o programa gh instalado, digite:
gh auth login
# Selecione autenticação via navegador
# Copie o código verificador
# Siga as instruções para autenticação
```


## 5. Fazer um fork deste repositório

Apenas **um** dos membros da dupla faz o fork deste repositório para sua conta github

Com o fork realizado, este membro da equipe deve inserir o outro membro como um colaborador do repositótio.  

## 6. Clonando o repositório nas máquinas locais

Para copiar um repositório existente para uma máquina local, usamos o `git clone`

Cada membro da equipe deve clonar o repositório para sua máquina

`git clone https://github.com/VOCE/SEU_FORK.git`

## 7. Fazendo alterações no projeto

Cada membro da equipe cria uma nova branch para trabalhar isoladamente

Para criar uma branch, use: 

```bash
# Cria a branch
git branch <nome_da_branch>

# Altera para a branch
git checkout <nome_da_branch>
```

Com o git setado para estar na sua própria branch, abra o projeto na IDE e siga as instruções:

- Copie o arquivo `_template.html`
- Altere o nome do arquivo. Um membro deve criar o arquivo `index.html` e o outro deve criar o arquivo `sobre.html`
- Insiram o conteúdo que quiserem dentro do espaço indicado


## 8. Versionando e atualizado

### COMMIT

Para salvar uma versão do nosso código, seguimos a sequência de ações:

```bash
# Antes de fazer um commit, verifique quais arquivos foram alterados com:
git status

# Para adicionar arquivos específicos à lista de arquivos do commit
git add <nome_do_arquivoA> <nome_do_arquivoB> 

# Para adicionar todos os arquivos modificados:
# git add .  

# Cria o commit com uma mensagem específica
git commit -m "Mensagem de commit personalizada"

# Criado snapshot do estado do código!
```


### PUSH

Para enviar suas alterações para o repositório remoto no GitHub:

`git push origin nome-do-branch`



### MERGE (com Pull Request)

Na página do seu repositório no github:

- Escolha a branch de origem (nome_do_branch)

- Escolha a branch de destino (geralmente main ou develop).

- Adicione um título e descrição para explicar o que foi feito.

Revise, ajuste e resolva conflitos, se necessário:

- Outros desenvolvedores revisam o código.

- Se solicitado, ajuste o código na branch de origem e envie novamente:

`git push origin nome_da_branch`

Mescle o Pull Request:

- Após aprovação, clique em "Merge" no GitHub.

### PULL

Atualize o seu repositório local com as atualizações que foram feitas no Github:

`git pull`


## 9. Lidando com conflitos de merge

Cada membro da dupla, em seu próprio computador e na sua branch, deve:

- abrir o arquivo `equipe.html`

- inserir uma pequena bio sobre si mesmo

- repetir todo o fluxo do tópico 8: 
     - commit
     - push
     - merge
     - pull

### Resolver conflitos de merge

Situação de conflito: Quando dois colaboradores alteram a mesma parte de um arquivo, um conflito pode ocorrer ao tentar fazer o merge.

Os conflitos podem ser revolvidos diretamente pelo github após o pull request!


## Extra 

Usando o arquivo .gitignore
