# Shell Study

## Comandos Básicos do Linux

### Arquivos e Diretórios

- pdw: qual diretório estou
- whoami: qual usuário logado
- ls: lista arquivos
- ls -l: - lista arquivos com informações adicionais
- echo: escreve na tela
- echo "texto" > arquivo.txt: cria arquivo com texto
- echo "texto" >> arquivo.txt: se o arquivo não existir, cria com texto, se existir, concatena texto no final
- cd: (change directory) entra em uma pasta
- cat: exibe o conteúdo de um arquivo
- mkdir: (make a dir) cria um diretório
- rmdir: apaga um diretório
- rm: apaga arquivo
- rm -r: apaga o diretório e sub-diretórios (recursivo)
- cp: copia arquivo
- mv: move arquivo
- zip -r test.zip pasta_ou_arquivos: zipa arquivos
- unzip -l text.zip: mostra o que tem dentro do zip
- unzip: descompacta zip
- tar -czf arquivo.tar.gz arquivo: compactação muito menor (recursivo por padrão)
- tar -xzf arquivo.tar.gz: compactação muito menor (recursivo por padrão)

### Parâmetros

- -r: recursivo
- -q: (quiet) executa comando e sai sem mostrar resultado
- -rq: exemplo de múltiplos comandos em um único parâmetro
- -l: listar
- -c: create
- -z: zip
- -x: extract
- -f: file
- -v: verbose (mais informações)

### Caracteres Coringa

- cat arquivo?.txt: qualquer caractere no lugar do ?
- cat arquivo*.txt: quaisquer caracteres (um ou mais) no lugar do *
- cat "arquivo*.txt": não considera caractere especial

### VI

- vi arquivo: entra no editor vi
- i: modo de insersão
- a: modo de insersão no caractere seguinte
- tecla esc: sai do modo de insersão
- :w : salvar
- :q : sair
- x: apaga caractere
- 3x: apaga 3 caracteres
- dd: apaga a linha
- :q! : sai sem salvar
- A: vai para o final da linha
