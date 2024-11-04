# ETL Pipeline de dados com python, biblioteca Requests e API do GitHub

O objetivo do projeto é desenvolver um pipeline ETL para extrair dados da API do GitHub das linguagens de programação mais utilizadas por grandes corporações ou de qualquer perfil de interesse, transformar, estruturar e carregar os dados para consumo.

O arquivo notebook contendo todo a linha de racionacio está disponível e também está disponível o mesmo código estruturado para ser reutilizado.

## 1° Extract
O projeto utiliza a biblioteca requests para extrair dados fazendo uma requisição do tipo GET a um usuário específico e listando todos os repositórios por meio da API do GitHub versão 2022-11-28 .

## 2° Transform
O projeto utiliza a biblioteca pandas para transformar e estruturar os dados obtidos da API do GitHub, após o processo é criando um arquivo CSV com os dados.

## 3° Load
Ainda com a biblioteca requests, o projeto cria um repositório fazendo uma requisição POST, e por fim carrega os dados no repositório fazendo uma requisição do tipo PUT na conta selecionada.

## Principais recursos e funcionalidades
1. Extração de dados com API
2. Trabalhar com Status Code
3. Autenticação
4. Paginação
5. Programação orientada e objetos

## Tecnologias Utilizadas
* Python
* Biblioteca Requests
* API GitHub
* Biblioteca Pandas

# Ambiente
O WSL2 permite ter acesso a um ambiente Linux completo, sem a necessidade de uma máquina virtual ou dual boot, além de permitir a integração com o sistema operacional Windows.

Para usar o WSL2 basta executar os seguintes comandos no windows powerShell do windows 10 ou 11 como adm:
```
wsl --list --online
```
Esse comando vai listar algumas versões do Ubuntu disponíveis para instalarmos.

Nós vamos instalar a distribuição "Ubuntu-22.04", para isso podemos executar o comando:
```
wsl --install -d Ubuntu-22.04
```

Após concluir a instalação, fechar o Windows PowerShell e abrir o terminal do WSL2

# Instalando pacotes
Antes de realizarmos a instalação de alguns pacotes Python, é importante atualizarmos os pacotes já instalados no WSL. Para isso, podemos abrir o terminal do WSL e executar os seguintes comandos:
```
sudo apt-get update
```

```
sudo apt-get upgrade -y
```

Feito isso, confira se você tem o Python instalado. Você pode fazer isso verificando a versão dele:
```
python3 -V
```

Agora, você pode instalar as bibliotecas pip e venv do Python:
```
sudo apt install python3-pip -y
```
```
sudo apt install python3-venv -y
```

# Criando um ambiente virtual
Um ambiente virtual Python é como uma caixa separada onde você pode instalar e gerenciar pacotes Python para um projeto específico, sem interferir em outros projetos ou no Python do sistema.

### Criando uma pasta para o projeto
```
mkdir projeto_Requests
```
### Acessando a pasta
```
cd projeto_Requests
```
Feito isso, podemos executar o comando para criação do ambiente virtual:
```
python3 -m venv venv
```
Em seguida, podemos ativar o ambiente:
```
source venv/bin/activate
```
E com o ambiente ativado, podemos instalar as bibliotecas que vamos utilizar no decorrer do nosso projeto:
```
pip install requests==2.28.2
```
```
pip install pandas==2.0.0
```

O editor de código é o VS Code instalado no Windows normalmente com a opção "adicione em PATH" ativada, após a instalação você instala a extensão do WSL2, python, jupyter.

Após tudo isso reinicie o PC e acesse a pasta do projeto, abra o VS dentro da pasta projeto via terminal com comando:
```
code .
```




