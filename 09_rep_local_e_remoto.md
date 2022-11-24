# Repositório local e remoto

Como o git é um sistema distribuído teremos uma versão dos nossos arquivos no servidor com o repositório remoto e na máquina pessoal com o repositório local.

As alterações que você na faz nos arquivos na sua máquina não repercute imediatamente no repositório remoto a menos que você configure de tal maneira.

- Servidor
    - Repositório remoto
- Ambiente de desenvolvimento
    - Diretório de tabalho/ Working Directory: que é o diretório onde estão nossos arquivos
    - Área de Staging: que é o local onde os arquivos estão se preparando para serem commitados
    - Repositório Local:

Os arquivos irão ficar transitando entre o diretório de trabalho e a área de staging  com o git add , untracked para staged, modified para staging….

Quando fazemos um commit ele irá para o repositório local que por sua vez pode ser empurrado para o repositório remoto com git push