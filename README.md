# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Nome do projeto - Um Mapa do Tesouro
![um_mapa_do_tesouro.jpg](https://github.com/IolandaManzali/IolandaManzali/blob/main/um_mapa_do_tesouro.jpg)

## Nome do grupo - Grupo 30

## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/in/hilmar-marques-358672161">Hilmar Gomes Marques da Silva</a>
- <a href="https://www.linkedin.com/in/iolanda-helena-fabbrini-manzali-de-oliveira-14ab8ab0">Iolanda Helena Fabbrini Manzali de Oliveira</a>
- <a href="https://www.linkedin.com/company/inova-fusca">Murilo Carone Nasser</a> 
- <a href="https://www.linkedin.com/in/pedro-eduardo-soares-de-sousa-439552309">Pedro Eduardo Soares de Sousa</a> 
- <a href="https://www.linkedin.com/company/inova-fusca">Yago Brendon Iama</a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/in/lucas-gomes-moreira-15a8452a">Lucas Gomes Moreira</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/company/inova-fusca">Andre Godoi Chaviato</a>


## 📜 Descrição
Esse repositório contem o modelo de dados para o projeto da atividade "UM MAPA DO TESOURO", proposta na segunda fase do curso de  Inteligencia Artificial da FIAP.

Essa atividade tem como objetivo a criação de um Modelo de Entidade Relacionamento (MER) e seu respectivo diagrama (DER) para a FarmaTech Solutions, utilizando a ferramenta Oracle SQL Data Modeler. 

Para desenvolver essa atividade foram considerados os seguintes aspectos:
 * Identificação das informações relevantes, levando em consideração o padrão multicultor, sensoriamento para umidade, pH e NPK, com monitoramento contínuo em tempo real das culturas. 
 * Criação das entidades e atributos, além da identificação da cardinalidade e tipação dos atributos, aplicando o SQL Data Modeler.

## Diagrama Entidade-Relacionamento (DER)

![der.rev_final](https://github.com/IolandaManzali/IolandaManzali/blob/main/der.rev_final.jpg)

### Entidades e Atributos

* **IMOVEL RURAL:**
  * CAR_IR (PK), NF_IR, LOC_IR, MED_IR
    
* **CULTURA:**
  * ID_CULT (PK), N_CULT, REG_CULT, DT_PLANTIO, MED_CULT, CAR_IR (FK)

* **SENSOR:**
  * ID_SS (PK), T_SS, LOC_SS, DT_INST, CAR_IR (FK), IS_LS

* **LEITURA DO SENSOR**
  * ID_SL (PK), DT_LS, RES_LS, ID_CULT (FK), ID_SS (FK)

## Modelo Entidade-Relacionamento (MER)

![mer.rev_final](https://github.com/IolandaManzali/IolandaManzali/blob/main/mer.rev_final.jpg)

 **Entidade IMOVEL RURAL:**
 ** Atributos:**
  * CAR_IR: CHAR, 43 caracteres
  * NF_IR: CHAR, 10 caracteres
  * LOC_IR: NUMBER, 40 caracteres
  * MED_IR: NUMBER, (6,2)
    
* **CULTURA:**
  * ID_CULT: NUMBER, 10
  * N_CULT: VARCHAR2, 7
  * REG_CULT: VARCHAR, 30
  * DT_PLANTIO: DATE
  * MED_CULT: NUMBER, (6,2)
  * CAR_IR: CHAR, 43

* **SENSOR:**
  * ID_SS: VARCHAR2, 10
  * T_SS: VARCHAR2, 10
  * LOC_SS: VARCHAR2, 30
  * DT_INST: DATE
  * CAR_IR: CHAR, 43
  * ID_LS: NUMBER, 8 

* **LEITURA DO SENSOR**
  * ID_SL: NUMBER, 8
  * DT_LS: DATE
  * RES_LS: NUMBER, (6,2)
  * ID_CULT: NUMBER, 10
  * ID_SS: VARCHAR2, 10

* **Legenda de Siglas**

* **CAR_IR:** Cadastro Ambiental Rural do Imóvel Rural
* **NF_IR:** Nome Fantasia do Imóvel Rural
* **LOC_IR:** Localização geográfica do Imóvel Rural
* **MED_IR:** Dimensao do imovel rural em hectares
* **ID_CULT:** Codigo de identificaçao da cultura
* **N_CULT:** Nome da planta (milho, soja ou café) 
* **REG_CULT:** codigo do registro do cultivar no MAPA
* **DT_PLANTIO:** data do plantio do cultivar
* **MED_CULT:** dimensão da area de plantio por cultivar
* **ID_SS:** codigo de identificação do sensor
* **T_SS:** tipo de sensor (umidade, pH ou NPK)
* **LOC_SS:** localização geografica do sensor
* **DT_INST:** data da instalacao do sensor no talhão
* **ID_LS:** codigo de identificção da leitura do sensor
* **DT_LS:** registro da data E hora da leitura do sensor
* **RES_LS:** registro do resultado da leitura do sensor 


## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>.github</b>: Nesta pasta ficarão os arquivos de configuração específicos do GitHub que ajudam a gerenciar e automatizar processos no repositório.

- <b>assets</b>: aqui estão os arquivos relacionados a elementos não-estruturados deste repositório, como imagens.

- <b>config</b>: Posicione aqui arquivos de configuração que são usados para definir parâmetros e ajustes do projeto.

- <b>document</b>: aqui estão todos os documentos do projeto que as atividades poderão pedir. Na subpasta "other", adicione documentos complementares e menos importantes.

- <b>scripts</b>: Posicione aqui scripts auxiliares para tarefas específicas do seu projeto. Exemplo: deploy, migrações de banco de dados, backups.

- <b>src</b>: Todo o código fonte criado para o desenvolvimento do projeto ao longo das 7 fases.

- <b>README.md</b>: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).

## 🔧 Como executar o código

### Pré-requisitos

Acesso ao software Oracle SQL Developer Data Modeler.

### Acesso ao projeto

Para acessar todo o conteudo do respositorio, incluindo arquivos de imagem utilize o comando abaixo pelo prompt Bash:

  * git clone https://github.com/IolandaManzali/IolandaManzali.git

Para baixar o arquivo desejado, digite o comando baixo no prompt do Bash ou curl:

Bash 
  * wget https://raw.githubusercontent.com/IolandaManzali/IolandaManzali/main/nome_do_arquivo.jpg

curl
  * url -O https://raw.githubusercontent.com/IolandaManzali/IolandaManzali/main/nome_do_arquivo.jpg

Para visualizar o arquivo diretamente no browser

  * abra o link abaixo em seu navegador https://github.com/IolandaManzali/IolandaManzali/blob/main/nome_do_arquivo_ou_repositorio
    
Obs: a criação do banco de dados ainda está em andamento. Disponibilizado somente a modelagem (logica e relacional)


## 🗃 Histórico de lançamentos

* 0.5.0 - XX/XX/2024
    * 
* 0.4.0 - XX/XX/2024
    * 
* 0.3.0 - XX/XX/2024
    * 
* 0.2.0 - XX/XX/2024
    * 
* 0.1.0 - XX/XX/2024
    *

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>


