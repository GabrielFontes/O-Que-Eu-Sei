# **Unix - Shell**

O Unix é um **sistema operacional** multi-tarefa. Denomidado por alguns como: "O pai de todos os sistemas operacionais". Vários outros sistemas operacionais utilizam o Unix como **padrão**. Um exemplo disso, é o Linux.

## **Características do UNIX**
  * **Multitarefa**: Várias tarefas podem ser executadas ao mesmo tempo.
  * **Multiusuário**: Vários usuários podem usar o computador simultaneamente. Vários terminais podem ser abertos ao mesmo tempo.
  * **Portável**: Por ser escrito em 'C', o Unix é um sistema fácil de modificar e transportar para outros computadores.

As primeiras versões do Unix, o "UNICS" era escrita em Assembly. Ou seja, cada arquitetura dependia de um código diferente. Já o Unix, tem um mesmo código em C que pode ser compilado para qualquer arquitetura.

## **Esquema do UNIX**
O Unix, assim como o Linux, é composto por, basicamente, três partes:

  - **Kernel**: O kernel é quem intermedia as relações entre as aplicações e o hadware do computador. É basicamente o núcleo do sistema operacional. RESPONSÁVEL POR INÚMERAS TAREFAS:
      - Gerenciar os processos;
      - Gerenciar arquivos;
      - Genrenciar recursos;
      - Entrada e saída de dados : Como os dispositivos podem ser compartilhados, a fiscalização impede problemas maiores;
 
  - **Shell**: Programa que interpreta os comandos digitados por um usuário e executa os programas. Pense em um diálogo entre duas pessoas que não falam a mesma língua. Faz-se necessário um intérprete. Esse é o Shell ! E os participantes do diálogo são O usuário e o kernel.

  - **Ferramentas**: Aplicações e ferramentas do sistema operacional.

## **Kernel**

## **Sistema de arquivos do Unix**
O sistema de arquivos descreve o tipo e a organização dos dados gravados no disco:

-  /**bin**: Guarda **comandos** binários essenciais para o sistema;
-  /**boot**: Guarda arquivos de **inicialização**;
-  /**etc**: Guarda os arquivos de **configurações** do sistema;
-  /**lib**: Guarda as **bibliotecas** necessárias para os comandos presentes no /bin e /sbin;
-  /**mnt**: Guarda as **partições** de dispositivos instalados;
-  /**opt**: Guarda **pacotes** não oficiais da distro;
-  /**dev**: Arquivos de entrada e saída;
-  /**usr**: Hierarquia secundária disponibilizada para todos os usuários;
-  /**home**: Diretório dos usuários

## **Shell - Alguns Comandos shell**

Existem vários tipos de shell. Cada shell tem as suas características, funcionalidades e pequenas variações de sintaxe, são exemplos de shell:

- **sh** (chamado Bourne shell);
- **bash** (Bourne again shell);
- **csh** (C Shell);
- **Tcsh** (Tenex C shell);
- **ksh** (Korn shell);
- **zsh** (Zero shell).

Abordarei comandos do bash

### **Comandos de navegação**

- '**cd**' - Navegar entre diretórios;

        cd [diretório]

- '**find**' - Localiza arquivos;

        find -[options] -name [expression]

<!-- '**grep**' - Busca strings em arquivos de texto específicos;-->
- '**ls**' - Lista os arquivos;

        ls -[options]
- '**mkdir**' -  Cria diretórios;
    
        mkdir [NomeDoDiretório]
- '**pwd**' -  Imprime a rota do local onde você está partido da raiz;
    
        pwd
- '**rm**' -  Exclui arquivos ou diretórios (Depende do parâmetro);

        rm -[options] [NomeDoArquivo]

### **Facilitadores**
- '**alias**'- Define um 'apelido' para os comandos;

        alias <Apelido do comando> = '< Comando >'

- '**unalias**' - Remove um alias;

        unalias <Apelido do comando>

### **Help**
- '**Man**' - Comando que mostra o manual de algum comando

        man <Comando>

### **Leitura de arquivos**
- '**cat**' - Imprime o conteúdo do arquivo na tela;

        cat <Nome do arquivo>

- '**echo**' - Exibe uma linha de texto/string na saída padrão ou em um arquivo.

        echo <string>
        echo <string> > <nome do arquivo de saída>

- '**head**' - Imprime as primeiras linhas de um arquivo;

        head <Nome do arquivo>

- '**less**' - Imprime o conteúdo do arquivo na tela;

        less <Nome do arquivo>

- '**tail**' - Imprime as últimas linhas de um arquivo;

        tail <Nome do arquivo>

### **Modificação de arquivos**
- '**bunzip**' - Decompactar ou compactar arquivos 'bz2'

  - Para compactar:

        bzip2 -z <Nome novo do arquivo>.bzip2 < Arquivo > 

  - Para descompactar:

        bzip2 -d <Nome novo do arquivo>.bzip2 < Arquivo > 

- '**chmod**' - Modifica permissões de arquivos e diretórios. Nesse caso, devemos saber sobre as permissões possíveis em um arquivo, e seus valores.

  - **R** = Permissão para leitura 
  - **W** = Permissão para escrita
  - **X** = Permissão para execução

O algoritmo usado no chmod é composto por três números e eles equivalem a binários transformados em números inteiros:

1º. Faz referência às permissões do dono do arquivo;\
2º. Faz referência às permissões do grupo do arquivo;\
3º. Faz referência aos outros usuários.

        chmod <Número das permissões> <Nome do arquivo ou diretório>

Fazendo relação com binário:
```
rwx/r-x/r-x
111/101/r-x
```
O Número da permissão nesse caso, seria 755

- **tar** - compactar ou descompactar um diretório 'tar.bz2'
  
  - Para compactar

        tar -cvjf arquivo.tar.bz2 pasta

  - Para descompactar
        
        tar -xvjf arquivo.tar.bz2


- '**gedit**' - Editar arquivos no bloco de nota;

        gedit <Nome do arquivo>

- '**gcc**' - Compilar programas em c;

        gcc <Nome do arquivo com o código> -o <Nome do executável>

- '**nano**' - Editar arquivos usando o nano;

        nano < Nome do arquivo>

- '**sed**' - Substituir caracteres em um arquivo de texto;



- '**tar**' - Decompactar arquivos 'tar/tar.gz'

- '**unrar**' - Descompactar arquivos 'rar'

- '**unzip**' - Descompactar arquivos 'zip'

### Especificação dos arquivos
- '**file**' - Imprime o tipo de um arquivo;

- '**wc**' - Mostra especificações dos arquivos (Quantidade de linhas, bytes, etc);

### **Processos**
- '**htop**' - Mostra processos que estão rodando;

- '**kill**' - Mata um processo que está rodando [xkill : mata o 
processo com o mouse];

- '**nice**' - Ajusta a prioridade de um processo;

- '**ps**' - Mostra processos que estão rodando;

- '**top**' - Mostra processos que estão rodando;


### **Usuários**
- '****' - 

- '**id**' - Identifica o usuário;

- '**last**' - Lista os ultimos usuários a se conectarem a máquina

- '**users**' - Imprime os nomes dos usuários logados no sistema;

- '**whoami**' - Identifica o usuário;

### **Especificações do sistema**
- '**uname**' - Mostra informações sobre o sistema (Sistema operacional, versão do kernel, arquitetura da máquina, etc);

- '**strace**' - Comando  no linux mostra o que há por baixo das system call's

### Transferindo arquivos entre servidores
- '**scp**' - Copiar arquivos via ssh;

        scp UserNoHost@HostQueEnviaráOArquivo:Path/Do/Arquivo/Que Será/Enviado Local/Para/Onde/Vai/O/Arquivo
