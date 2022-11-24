# Criando um repositório remoto e fazendo um commit

Para criarmos um repositório remoto primeiramente precisamos ter um repositório localmente com os arquivos do projeto lá dentro.

O próximo passo é no terminal, temos que navegar até a pasta do repositório local e rodar os seguintes comandos:

Esse comando serve para indicar que aquele diretório é um repositório git e a partir de agora ele poderá ser gerenciado pelo git e não é necessário caso o repositório local foi clonado com git clone:

```bash
git init
```

Depois temos que enviar as alterações que ocorreu no repositório para uma área temporária chamada Stage que é uma área onde fica salvo as alterações que deverá ser feita no próximo commit.

(No caso de repositórios sendo criado as alterações serão apenas de arquivos novos, porém em repositórios já existentes terá arquivos modificados, deletados, renomeados..) 

Isso com o seguinte comando:

```bash
git add .
```

o ‘.’ faz referência a todos os arquivos do repositório, porém podemos adicionar apenas um arquivo:

`git add nomeArquivo`

Com esse comando conseguimos verificar os Status de modificações que será feita no repositório remoto:

```bash
git status
```

Trocamos para a branch 

Após adicionarmos as alterações no campo Stage temos que comunicar as alterações ao Git com o commit

Se você está iniciando esse repositório é necessário criar um novo repositório remoto no github e depois  temos que vincular o repositório local e remoto com o comando:

(Caso o repositória já existe e foi clonado com git clone não é necessário vincular)

```bash
git remote add origin git@github.com:seuusuario/seurepositorio.git
```

Depois precisamos enviar os arquivos ao repositório remoto com o comando:

```bash
git push -u origin main
```

Caso esteja fazendo um commit faça os seguintes passos:

```bash
git add .
git commit -m "Um comentário qualquer"
git push
```