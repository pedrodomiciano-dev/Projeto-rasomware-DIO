# Laboratório de Criptografia em Python

## Sobre o projeto

Esse projeto se trata sobre um desafio da DIO, do qual, devo usar o Kali Linux para a criação de scripts em Python para criptografar e descriptografar um arquivo de texto, buscando ter uma melhor compreensão de como funciona e de como usar o Ransomware em um ambiente controlado


## Tecnologias

- Python
- pyaes
- Kali Linux
- Oracle VirtualBox

## Arquivos principais

- `encrypter.py`: armazena o código para critografia
- `decrypter.py`: armazena o código para descriptografia
- `teste.txt`: arquivo responsável por armazenar o texto e testar scripts

## Como executar

Este projeto foi desenvolvido no Kali Linux, executado em uma máquina virtual (VM) por meio do Oracle VirtualBox.

Como as configurações do ambiente podem variar entre usuários, esta seção apresentará os requisitos e os comandos necessários para preparar o ambiente Python e executar os scripts, incluindo possíveis soluções para problemas de dependências.

-----

## 1 - Crie uma pasta e arquivos

Dentro do terminal do Kali Linux, deve ser criar e entrar em uma pasta, então use:

```
mkdir projeto-ransomware
cd projeto-ransomware
```
Após criar e entrar na pasta digite os seguintes comandos:

```
nano encrypter.py
nano decrypter.py
nano teste.txt
```
A estrutura final deve ficar assim:

```
projeto-ransomware/
├── encrypter.py
├── decrypter.py
├── teste.txt
└── README.md
```
Com isso, copie e cole os scripts desse repositório em seus respectivos arquivos criados, acessando via `nano` no terminal, colando os scripts salvar com `Ctrl + O`, depois `Enter` e por `Ctrl + X`

## 2 - Criar ambiente python

Caso você tente executar por exemplo `python encrypter.py` e aparecer uma mensagem de erro, isso pode significar que o Kali não baixou todos os pacotes necessários, nesse caso digite os seguintes comandos dentro da pasta:
```
python3 -m venv .venv
source .venv/bin/activate
```
Após isso, instale a bilbioteca:
```
python -m pip install pyaes
```
Se o comando venv não estiver disponível, instale o pacote correspondente no Kali:
```
sudo apt update
sudo apt install python3-venv
```
E para conferir a estrutura:
```
ls -la
```





## Aprendizados

## Aviso de segurança

Este projeto possui finalidade educacional e foi desenvolvido em um ambiente de testes controlado, logo, não deve ser utilizado para criptografar arquivos de terceiros ou dados sem autorização.
