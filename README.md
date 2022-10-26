# Comandos Principais GIT

## git clone

Esse comando é utilizado para baixar repositórios existentes, seja no GitHub ou qualquer outra plataforma que usa GIT, mas esse download é feito de forma local dentro da sua máquina.

### Como utilizar

```bash
git clone <url_do_projeto>

# Exemplo
git clone https://github.com/guscsales/thon-ui.git
```

## git init

O principal comando para inicializar o git é o `git init`. Ao executar esse comando uma pasta chamada `.git` é criada no diretório onde ele foi executado e nessa pasta você pode fazer o link para a origem (origin) remota, que pode ser o GitHub, GitLab, Bitbucket ou qualquer outra plataforma que utilize o Git.

### Como utilizar

```bash
git init
```

## git add

Esse comando vai transportar todos os arquivos, sejam novos ou modificados para um lugar chamado "stage”. Podemos adicionar arquivo por arquivo, ou então todos de uma vez.

### Como utilizar

```bash
git add <. ou arquivo ou pasta>

# Adicionando todos os arquivos e pastas
git add .

# Adicionando um arquivo
git add index.html

# Adicionando uma pasta
git add assets
```

## git status

Com ele nós conseguimos ver o que está no "stage” e o que não está, também se um arquivo será adicionado ou deletado. Assim fica mais claro entender o que vai para o commit e o que não vai para o seu commit.

### Como utilizar

```bash
git status
```

## git commit

O `git commit` cria para você um registro com uma mensagem daquilo que você jogou em "stage” através do comando `add`.

### Como utilizar

```bash
git commit -m <mensagem_do_commit>

# Exemplo
git commit -m "feat(auth): create login screen"
```

**Dica: Para uma melhor organização é interessante utilizar os padrões de commit chamados [Conventional Commits (Link Oficial)](https://www.conventionalcommits.org/en/v1.0.0/) você também pode ler o artigo em português ["Conventional Commits Pattern"](https://medium.com/linkapi-solutions/conventional-commits-pattern-3778d1a1e657) escrito por Victor Ribeiro.**

## git push

Esse comando faz com que todos os nossos commits sejam empurrados (tipo um upload) na origem do repositório, poe exemplo, dentro do GitHub. Ao executar com o `-u` você está dizendo que essa branch faz parte de um repositório remoto, o `-u` é uma abreviação para o `--set-upstream`.

Não será necessário utilizar o `-u` o tempo todo, apenas quando novas branches forem criadas para joga-las no provedor Git.

Caso o `git push` seja executado sem o `-u` será necessário sempre informar a origem e o nome da branch para que as alterações sejam levadas ao provedor Git.

### Como utilizar

```bash
# Na primeira vez
git push -u origin <nome_da_branch>

# Nas outras vezes
git push

# Quando executado sem -u
git push origin <nome_da_branch>
```

## git pull

Ao rodar esse comando em qualquer branch, seja na main ou em outra, você consegue pegar a última versão que está na origem remota, ou seja, todos os novos commits das pessoas que trabalharam naquele projeto vai diretamente para a branch em questão.

Uma nota importante, se você fez um push com -u em algum momento, apenas um git pull dentro da branch será necessário, mas caso você não tenha feito isso, para baixar as atualizações será necessário rodar um git pull com `origin <nome_da_branch>`.

### Como utilizar

```bash
git pull

# Se precisar buscar na origin, quando não foi feito `git push -u`
git pull origin <nome_da_branch>
```

## git checkout

O git checkout acessa branches, ou seja, ramificações existentes (locais ou remotas) e também cria uma nova branch a partir de outra que você já esteja, quando acompanhado do `-b` em sua execução.

As branches normalmente são utilizadas para criar novas features sem precisar afetar a principal, ou seja, a branch `main` (na maior parte dos casos).

### Como utilizar

```bash
git checkout <nome_da_branch>

# Para criar uma nova branch
git checkout -b <nome_da_branch>
```

## git branch

Lista todas as branches locais ou remotas, também delete branches locais.

### Como utilizar

```bash
git branch

# Para deletar uma branch local
git branch -D <nome_da_branch>

# Para deletar uma branch remota
git push --delete origin <nome_da_branch>
```

## git rebase

Esse comando alinha todos os commits de uma branch, seja a principal ou qualquer outra que você escokher na branch atual em que você está localizado, porém sem criar um novo commit, como faz o `git merge`, mantendo o histórico linear.

### Como utilizar

```bash
git rebase <nome_da_branch>

# Exemplo, você atualmente está na branch "tela-de-login"
git rebase main
```

## Links

- Vídeo no YouTube: "Principais Comandos Git que TODO Dev Precisa Saber" (Em Breve)

## Me Siga nas Redes Sociais!

[![Twitter](https://gsales.io/social-media-icons/twitter.png)](https://twitter.com/guscsales)
[![Instagram](https://gsales.io/social-media-icons/instagram.png)](https://www.instagram.com/guscsales/)
[![YouTube](https://gsales.io/social-media-icons/youtube.png)](https://canal.gsales.io)
[![LinkedIn](https://gsales.io/social-media-icons/linkedin.png)](https://www.linkedin.com/in/gsaless/)
[![Personal Website](https://gsales.io/social-media-icons/site.png)](https://gsales.io)
