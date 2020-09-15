# GIT Iniciante
Assim que eu entrei na Aptans, tive que me adaptar aos métodos de trabalho que eram utilizados. Apesar de não ter tido práticas anteriores, consegui me adaptar e tenho buscado a excelência. O meu primeiro tópico de estudo foi o Git. Minha intenção é que a partir dessa postagem o leitor seja capaz de executar os comandos básicos e entender um pouco sobre a estrutura desse sistema de versionamento.

## **O'que é GIT?**
  O git é um sistema de versionamento distribuído. 

> Mas, o'que exatamente isso quer dizer? 

Quer dizer que várias pessoas conseguem ter acesso a um mesmo documento e alterá-lo simultaneamente de forma segura.
  
  Um ponto válido para ressaltar é que existem vários métodos diferentes de aplicar o git a um projeto justamente porque as formas de organização variam. No git existem **branchs** (que são linhas de desenvolvimento) a **branch master** é a principal normalmente, nela existem as versões de *produção*. Outras Branchs podem ser usadas para isolar a versão de produção para resolver algum erro ou abordar um problema de forma diferente.

## **Por que usar o git?**
     
Uma vez que as edições podem ser feitas simultaneamente e existe uma cópia remota do projeto no computador de cada pessoa envolvida, esse sistema gera **velocidade de produção** e muita **segurança**.

## **Como funciona o git?**
    
O git utiliza alguns **objetos de rastreamento e grafos** que são basicamente, um conjunto de elementos relacionados para armazenar os dados e acrescentar ao arquivo, somente o que foi alterado. Os objetos são:

 - **Blob**: Objeto de rastreamento dos arquivos e é representado por um heash. É apontado pelo Tree.
 - **Tree**: Objeto que relaciona o commit com o blob. Ele é apontado pelo commit e aponta para o Blob.
 - **Commits**: Mensagem informando o que está sendo feito. É representado assim como o blob, por um heash e aponta para o Tree. 

# **Abordagens mais práticas**
        
Existem três áreas de atuação no git. São elas:

 - **working directory**: É o diretório local monitorado pelo git (repositório local);
 - **Staging area**: Aqui ficam os arquivos preparados para o commit;
 - **Repository**: Arquivos prontos para o repositório remoto.

Existem várias plataformas/sites que usam o git para o controle de versão dos códigos. Para ter um repositório de trabalho listarei alguns possíveis comandos seguidos por suas explicações. Eles serão divididos em:
- **"Iniciando um repositório"**\
  Contém os comandos para a criação do repositório
- **"Manutenção do repositório local"**\
  Para chegar a esse ponto, devemos ter um diretório local pronto.
- **"Mandando para o repositório remoto"**\
  Esse é o momento que as alterações já estão prontas para serem mandadas para o repositório remoto.
        
# **Comandos**
## **Iniciando um repositório**
```
git clone <link do repositório>
```
- Esse comando **clona o repositório remoto na máquina local** acrescentando o sub-diretório `.git` ao local onde o comando foi executado. 

```
git init
```

- Enquanto no git clone, iniciamos o repositório na plataforma e depois linkamos ao nosso computador, com o git init, **iniciamos o repositório na máquina local e depois linkamos ao repositório da plataforma**.

```
git remote add < nome do remoto > < link >
```

- Define o repositório remoto que será linkado ao seu repositório.

## **Manutenção do repositório local**

 Para ajudar na compreensão, *imagine um porto marítimo repleto de **containers** vazios, **placas de rastreamento**, **caminhões** cheios de **televisores** para colocar nesses containers e **navios** prontos para serem carregados*.

 - Os caminhões carregados são o **Working directory**;
 - Os televisores são os **arquivos**;
 - Os containers a **staging area**;
 - As placas de rastreamento os **commits**;
 - O navio, o **repository**.

Os comandos principais nesse ponto, são:

```
git add < nome do arquivo alterado >
```

- O git add é responsável por mandar os arquivos do Working Directory para a Staging area. Usando a analogia anterior, esse comando colocaria os televisores (Arquivo) dentro do container.

```
git branch < nome da branch >
```

- Cria um novo "ramo" de trabalho. Imagine que surgiu um erro e você não quer atrapalhar o andamento do projeto. Crie um **"branch"**, trate o erro e depois faça um **"merge"** (Juntar a branch ao ramo master).

```
git commit < nome do arquivo que será comentado >
```

- Paralelamente ao "git add", o git commit prepara os arquivos para o repository rotulando-os com mensagens. Usando a analogia do porto marítimo, o git commit seria as placas de rastreamento anexadas aos containers.

```
git diff < branch >
```

- Mostra as alterações feitas no branch.

```
git fetch
```

- Ele atualiza as referências locais com relação às remotas, mas não faz o merge com o branch local.

```
git merge < bual branch você vai mergir >
```

- Consiste em pegar as alterações de um branch e aplicar em outro. Nesse ponto é importante saber qual branch você está. Se o comando é usado na master, o merge vai ser para a master.

```
git pull
```

- Pega as modificações do repositório remoto e aplica no repositório local 

```
git reflog
```

- Esse comando mostra os ultimos comandos que foram executados no repositório.

##  **Mandando para o repositório remoto**

```
git push < para onde > < qual branch >
```
- Esse comando pega todos os arquivos da Staging area e manda para o servidor remoto.