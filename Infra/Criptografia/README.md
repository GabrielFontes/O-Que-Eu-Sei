# Segurança da Informação

## **O que é segurança?**

Segurança é um **estado** e deve ser sempre atualizada.

    Segurança da informação é muito valorizado


## **Propriedades fundamentais da segurança da informação**

São três propriedades:

- **Confidencialidade**: Somente quem deveria ter acesso, tem acesso. Garantir o acesso a quem deve ter acesso;

        Como?
        Restringindo o acesso ao meio por onde as mensagens passarão.
        Na computação, um método: Criptografia.

- **Integridade**: Algo inteiro, completo, não sofreu diminuição, garante que uma informação esteja correta;

        Como?
        Na computação: Usar um meio de comunicação confiável, mídia de armazenamento confiável; 

- **Disponibilidade**: Acessível quando for necessário;


## **Formas de tentar garantir a segurança**

### **Criptografia**
Esconder através de "cifras" alguma informação. É usada tanto pra armazenamento quanto na transferência de dados. Antes de falar sobre as formas de criptografia, devo abordar alguns conceitos:

 - **Texto claro**\
    Texto antes de ser cifrado/encriptado;
 - **Algoritmo de encriptação ou chave ou cifra** :\
    Regra usada para cifrar/encriptar;

 - **Texto cifrado**:\
    Texto "embaralhado";

 - **Algoritmo de desencriptação**:\
    Algoritmo usado para desembaralhar/desencriptografar o texto cifrado.
 
Existem dois tipos de criptografia:

#### **Criptografia Simétrica** 
Existem um compartilhamento do algoritmo de encriptação ou, na computação, **compartilhamento de chaves**. 

    Exemplo:
    Cifra de Cesar : Deslocação das Letras (Técnica de transposição simples)
            oi -> qk

```
Porque chamamos de Criptografia Simétrica?
Pois a mesma chave é usada para encriptografar e desencriptografar o arquivo.
```

- **Problema:**\
    Como transmitir a chave para o receptor?\
    Se a chave for pedida, todos que tiverem a chave, terão acesso a tudo.

- **Solução:**\
    É só criptografar com outra chave! :x 

Pensando exatamente nisso, foi criada a **Criptografia Assimétrica**.


#### **Criptografia Assimétrica**

Aqui existem duas chaves. Uma para ciptografar ou assinar os dados e outra para descriptografar.

- **Chave privada:**\
    Só o detentor da chave, tem acesso.
- **Chave Pública:**\
    Qualquer pessoa pode ter acesso.

As chaves tem relação entre si.

- O que a **chave pública ciptografa**, com a **chave privada consegue desencriptografar**.
- O que a **chave privada criptografa**, com a **chave pública é possível desencriptografar**.

Por esse motivo, a **Chave Privada** é usada para **assinar dados** e a **Chave Pública** é usada para **criptografar**.

Usarei alguns exemplo para explicar.

1. Vou acessar um site (Que usa HTTPS). Quando realizo o acesso, ele me manda uma cópia da chave pública.
2. O cliente **cria uma chave simétrica** e criptografa os dados;
3. O cliente **criptografa a chave simétrica com a chave pública do site**
4. O site recebe a **chave simétrica criptografada** e **usando a chave privada**, desincriptografa.

A criptografia assimétrica tende a ser mais lenta.