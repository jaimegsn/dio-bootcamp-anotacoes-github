# Git : Instalação no sistema e configuração

### Instalação:

[https://git-scm.com](https://git-scm.com/)

Basta ir na aba downloads e baixar de acordo com o seu sistema operacional.

---

### Instalação:

Agora vamos configurar no terminal a sua identificação para poder utilizar o versionamento do git ( necessário ter uma conta github)

Apesar de poder ser feito no terminal normalmente do sistema, é melhor utilizar o programa Git Bash que foi instalado anteriormente se estivermos no windows.

Primeiramente informamos nosso username:

```bash
git config --global user.name "SeuUsername"
```

Depois informamos o email:

```bash
git config --global user.email "seuemail@gmail.com"
```

E pronto está configurado, para conferir digite o comando:

```bash
git config --list
```

e confira os 2 últimos campos

---

Uma configuração para usuários de windows é permitir a visualização de arquivos ocultos, para facilitar e podermos visualizar a pastar .git do repositório local.

Para isso pesquisaremos e acessaremos no menu iniciar as “opções do explorador de arquivos”

Na janela das opções do explorador de arquivos iremos na aba “Modo de exibição”

e marcaremos a opção: “Mostrar arquivos, pastas e unidades ocultas”

e desmarcaremos a opção: “Ocultar as extensões dos tipos de arquivo conhecidos”