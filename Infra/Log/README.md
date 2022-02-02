# Log
Ainda seguindo meu anseio maior no estágio de ser um grande SysAdmin, me foi proposto estudar sobre Log. Fiquei impressionado depois de descobrir que encontrar a causa de um erro na área da computação pode ser uma coisa tão simples.

## O que é log?
É uma 'documentação' automaticamente produzida contendo registros de data e hora de eventos relevantes para um sistema específico. Interessante ressaltar que os arquivos de log nunca são sobrescritos.

## Qual a finalidade do log?
Através das análises é possível fazer a detecção rápida de falhas, fazer estudo de padrões de uso a partir do número de solicitações para cada página e pelo número de visitantes, aumentar a conscientização de segurança.

## Como funciona?
Cada frase escrita no log é rotulada com seu nível que pode são:
- **Debug**: Mensagens de depuração do programa;
- **Info**: Mensagens de informação;
-  **Notice**: Não chegam a ser erros mas merecem atenção;
- **Warning**: Mensagens que necessita de solução;
-  **Crit**: Mensagens críticas (erro de hardware).

E são guardados normalmente no diretório /var/log. Os principais arquivos são:
    
        apt/
Diretório com logs de uso do gerenciador de pacotes apt-get
    
        boot.log
Registro dos serviços carregados durante a inicialização do sistema;

        dmesg

Log do último boot (processo de arranque ou inicialização do computador durante o carregamento do sistema operacional quando a máquina é ligada)

        auth.log
Armazena logs de autenticação, incluindo logins e métodos de autenticação bem-sucedidos e com falhas.
    
        kern.log
Mensagens detalhadas do kernel do Ubuntu Linux;

        syslog
            
Mensagens do Ubuntu Linux que não foram armazenadas em logs mais específicos. Consulte-o quando você não achar a mensagem desejada em outros arquivos;

        Xorg.0.log
Informações sobre drivers da placa de vídeo e o ambiente gráfico.  

Além desses, existem alguns outros logs de programas que podem ser encontrados dispostos nesse mesmo diretório ou em sub-diretórios que facilitam a detecção de falhas.
    
## Alguns Comandos 
Alguns comandos para vizualisar os arquivos de log são:
    
        less
Mostra todo o arquivo de log e com alguns parâmetros é possível limitar isso. (-n, por exemplo)

        head
Mostra linhas (limitadas) a partir do cabeçalho.

        tail
Mostra as linhas finais do arquivo.

Um parâmetro muito interessante é o "-f", ele permite visualizar em tempo real as alterações sofridas por um arquivo de log. Por fim, vale dizer que existem ferramentas como o 'Retrace' ou o 'DataDog' que possibilitam a reunião dos logs para facilitar o monitoramento nos servidores. 

Posteriormente, acrescentarei meus flash card para estudo, disponibilizarei os conteúdos no meu [site](fontes.aptans.com) e acrescentarei informações sobre assuntos relativos a TI. Obrigado pela atenção.