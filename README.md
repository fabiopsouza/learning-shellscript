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
- tar -czf arquivo.tar.gz arquivo: compactação muito menor e também manter as permissões (recursivo por padrão)
- tar -xzf arquivo.tar.gz: compactação muito menor (recursivo por padrão)
- locate nome: procura o nome no HD (tem banco de dados com caminhos que é atualizado de tempo em tempo)
- updatedb: atualiza o banco de dados do locate
- which comando: exibe qual arquivo será executado quando rodar o comando
- env: exibe as variáveis de ambiente
- PATH=$PATH:diretorio : acrescenta o diretório no path
- ~/ : equivalente a home

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

### VIM (Sucessor VI. Comandos do VI também funcionam)

- vim: abre o editor
- vim arquivo: abre o arquivo no vim
- :echo $HOME (dentro do vim): mostra em qual pasta vim vai ler arquivo de configuração
- vim .vimrc: cria arquivo de configuração do vim
- 10 comando: repete o comando 10x (Ex.: 10 seta para esquerda)
- j: seta para baixo
- k: seta para cima
- h: seta para esquerda
- l: seta para direita
- /nome_a_procurar: procura no arquivo
- n: vai para a próxima ocorrência da busca
- shift n: vai para a ocorrência anterior
- u: desfaz última alteração
- ctrl r: volta as alterações desfeitas
- o: modo de insersão na próxima linha
- SHIFT o: modo de insersão na linha acima
- :%s/ul/nav/g : muda palava ul para nav globalmente (g)
- :%s/ul/nav/gc : muda palava ul para nav globalmente escolhendo com Yes e No (gc)
- shift+v: modo de seleção de linhas
- ctrl+v: modo de seleção por bloco
- y: copiar
- p: colar
- == :  ajusta a identação da linha
- :vs nomeArquivo (vertical split): abre o outro arquivo dividindo a tela na vertical
- :sp nomeArquivo (split padrão horizontal): abre o outro arquivo dividindo a tela na horizontal
- Ctrl + WW: transita entre os arquivos splitados
- Ctrol + W + H: Vai para o split da esquerda 
- Ctrol + W + L: Vai para o split da direita

### Programas, Processos e Pacotes

- ps: exibe processos do terminal
- ps -e: exibe todos os processos do linux
- ps -ef: exibe processos com mais detalhes
- kill numero_do_PID: mata o processo com aviso
- kill -9 numero_do_PID: mata sem avisar
- ps -ef | grep nome: redireciona o resultado para o grep procurar
- top: lista os processos e seu consumo
- killall nome: mata todos os processos pelo nome (sem PID)
- pstree: mostra os processo em árvore
- jobs: processos que estão rodando
- bg numero_do_job: passa o job para background (sem número pega o primeiro)
- fg numero_do_job: tira do background (sem número pega o primeiro)
- nome_processo &: abre em backgroud direto
- sh nome_script: roda o script
- sudo apt-get update: atualiza os programas disponíveis para instalação
- apt-cache search ftp: procura programas relacionados a ftp por exemplo
- sudo apt-get install nome_programa: instala um novo programa
- wget endereço: baixa arquivos/páginas da web
- sudo dbkg -i nome.deb: instala um programa baixado manualmente, fora da relação do linux
- sudo service nome_servico stop: para serviço
- sudo service nome_servico start: inicia serviço
- make (dentro da pasta do programa baixado): instala um programa a partir do código fonte. Vai informar se tiver dependência faltando

### Permissões

- d: diretório
- r: leitura
- w: escrita
- x: execução
- arquivo -rwx -rw- -r-x: primeira coluna dono, segunda grupo e terceira outros
- chmod +x nome_arquivo: acrescenta permissão de execução ao arquivo
- chmod -x nome_arquivo: remove permissão de execução ao arquivo
- chmod u-r: tira permissão do usuário
- u: usuário
- g: grupo
- o: outros 
- sudo comando: executa comando com o usuário root
- passwd: muda a senha do usuário
- sudo passwd: muda a senha do usuário root
- su nome_usuario: logar um um usuário específico
- adduser nome: cria um usuário novo
- exit: desloga do usuário

### Plugins

https://github.com/tpope/vim-pathogen


### Outros

- scripts dentro do diretório /etc/init.d serão executados no start
- ssh-client: programa para logar em outra máquina
- ssh-server: programa para servir como servidor
