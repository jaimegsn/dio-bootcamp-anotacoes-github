# Como o Git Funciona

- SHA1 (Secutiry Hash Algoritm)
    
    É um algoritmo de encriptação, a grosso modo ele irá criptografar os seus arquivos (foto/texto/video…), ele irá embaralhar esse arquivo de uma forma específica gerando um conjunto de 40 caracteres identificadores únicos.
    
    Quando alteramos o conteúdo do arquivo é gerado um novo identificador.
    Comando para gerar a criptografia de um arquivo: openssl sha1 arquivo.txt
    O SHA1 não encripta apenas os seus arquivos mas também os objetos internos do GIT
    

- Objetos Internos Fundamentais do GIT
    - BLOBS
        
        O Blob contém meta dados do git como tipo do objeto, tamanho do arquivo e etc.. todos esses meta dados são criptografados com SHA1
        
    - TREES
        
        As Trees apontam para outras trees e para blobs, elas armazenam meta dados responsáveis por localizar os arquivos, meta dados do SHA1 do arquivo e do nome do arquivo.  As Trees também são criptografados com SHA1
        
    - COMMIT
        
        É o objeto que vai juntar tudo, ele aponta para uma Tree, ele aponta para um parente ou seja o último commit realizado antes dele, aponta para um autor, aponta para uma mensagem.  E o commit todo representa uma alteração feita nos arquivos.  Os Commits também são criptografados com SHA1
        
    
    Ou seja se alterarmos um arquivo do Blob é alterado o SHA1 do blob e o SHA1 da árvore que está apontando para o blob que por sua vez altera o SHA1 do commit