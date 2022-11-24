# Chave SSH

Quando formos salvar arquivos no github precisamos nos autenticar, geralmente isso acontece por meio de login e senha, porém com a finalidade trazer mais segurança o github mudou a forma de autenticação, agora ela é feita através de uma chave SSH, geramos uma chave SSH do computador e autorizamos aquele computador á poder fazer operações na conta GIT. (porém ainda é possível utilizar o método de login e senha)

Para gerarmos uma chave SSH digitaremos o código no terminal:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"

caso der erro use esse -> ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Depois ele gerará a chave SSH mostrando o seguinte feedback:

 Output → `Generating public/private *algorithm* key pair.`

Depois irá pedir para digitarmos qual pasta queremos salvar a chave:

 Input → `Enter a file in which to save the key (/c/Users/*you*/.ssh/id_*algorithm*):`
se não digitarmos nada e apertar ENTER ele salvará na pasta do sistema (É o que eu faço)

Irá aparecer um feedback do diretório:

 Output → `Created directory '/c/Users/Usuario/.ssh'.`

Depois será solicitado uma senha, essa senha posteriormente será cobrada para as operações no git, útil para casos em que mais de uma pessoa tem acesso a máquina, você pode digitar nada também:
Input → `Enter passphrase (empty for no passphrase):`

Confirme a senha:

Input → `Enter same passphrase again:`

Irá aparecer a confirmação da chave SSH.

Você pode ir no arquivo e abrir com um editor ou no proprio CLI ir no diretório `(/c/Users/*you*/.ssh/)`  e digitar o comando  `cat id_xxxx*.pub*`

Depois temos que registrar a chave SSH nas configurações do github:

Settings → SSH and GPG Keys → New SSH Key

Preencher com um titulo e preencher com a SSH Key publica e não a privada, depois é só e salvar.

As SSH Keys estarão na pasta ‘.ssh’

Agora precisamos inicializar o SSH AGENT que é o responsavel por lidar com as chaves SSH

precisamos digitar esse comando: `eval $(ssh-agent -s)`  dentro no CLI dentro do diretório: `(/c/Users/*you*/.ssh/)`

Agora ainda dentro do diretório .ssh precisamos informar nossa chave privada ao ssh agent com o comando: `ssh-add id_xxxx` 

Depois disso irá aparecer um feedback de que a chave foi adicionada, algo parecido com isso:

Identity added: id_xxxx (you_mail@example.com)

Agora quando formos usar o comando git clone em repositórios privados precisamos utilizar a URL SSH