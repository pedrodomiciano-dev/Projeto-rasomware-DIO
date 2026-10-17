# Laboratório de Criptografia em Python

## Sobre o projeto

Este projeto foi desenvolvido como parte de um desafio da DIO. O objetivo é utilizar o Kali Linux para criar scripts em Python capazes de criptografar e descriptografar um arquivo de texto, buscando compreender melhor o funcionamento da criptografia de arquivos e sua relação com ataques do tipo ransomware em um ambiente controlado.

## Tecnologias

- Python
- pyaes
- Kali Linux
- Oracle VirtualBox

## Arquivos principais

- `encrypter.py`: contém o código responsável pela criptografia do arquivo.
- `decrypter.py`: contém o código responsável pela descriptografia do arquivo.
- `teste.txt`: arquivo de texto utilizado para testar o funcionamento dos scripts.

## Como executar

Este projeto foi desenvolvido no Kali Linux, executado em uma máquina virtual (VM) por meio do Oracle VirtualBox.

Como as configurações do ambiente podem variar entre usuários, esta seção apresenta os requisitos e os comandos necessários para preparar o ambiente Python e executar os scripts, incluindo possíveis soluções para problemas relacionados às dependências.

### 1. Criação da pasta e dos arquivos

No terminal do Kali Linux, crie uma pasta para o projeto e acesse-a utilizando os seguintes comandos:

```bash
mkdir projeto-ransomware
cd projeto-ransomware
```

Em seguida, crie e abra os arquivos utilizando o editor de texto `nano`:

```bash
nano encrypter.py
nano decrypter.py
nano teste.txt
```

Copie os scripts deste repositório e cole cada um no arquivo correspondente. Para salvar o conteúdo no `nano`, pressione `Ctrl + O`, confirme com `Enter` e, em seguida, pressione `Ctrl + X` para sair do editor.

A estrutura final do projeto deverá ser semelhante a esta:

```text
projeto-ransomware/
├── encrypter.py
├── decrypter.py
├── teste.txt
└── README.md
```

O arquivo `README.md` contém a documentação do projeto. Ele também deverá estar presente na pasta do projeto.

### 2. Preparação do ambiente Python

Antes de executar os scripts, verifique se o Python 3 está instalado:

```bash
python3 --version
```

Para criar um ambiente virtual e ativá-lo, execute os seguintes comandos dentro da pasta do projeto:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

O ambiente virtual permite isolar as dependências Python utilizadas pelo projeto.

Em seguida, instale a biblioteca `pyaes`:

```bash
python -m pip install pyaes
```

Caso ocorra um erro informando que o módulo `venv` não está disponível, instale o pacote correspondente no Kali Linux:

```bash
sudo apt update
sudo apt install python3-venv
```

Após a instalação, tente criar e ativar o ambiente virtual novamente.

Para conferir os arquivos presentes no diretório, incluindo os arquivos e pastas ocultos, execute:

```bash
ls -la
```

**Observação:** erros durante a execução dos scripts podem ter diferentes causas, como dependências ausentes, caminhos incorretos ou problemas no código. Portanto, verifique a mensagem de erro antes de determinar a solução.

Acesse a pasta do projeto:
```
cd ~/projeto-ransomware
```
Ative o ambiente virtual, caso ainda não esteja ativado:
```
source .venv/bin/activate
```
Confira os arquivos existentes:
```
ls -la
```
Antes de executar os scripts, confirme que os nomes dos arquivos e os caminhos definidos no código correspondem aos arquivos presentes no diretório.

Execute o script de criptografia:
```
python encrypter.py
```
Verifique o resultado e, em seguida, execute o script de descriptografia:
```
python decrypter.py
```
Por fim, confira se o arquivo recuperado contém os mesmos dados do arquivo original.

## Aprendizados

[Descreva os conceitos técnicos que você aprendeu durante o desenvolvimento do projeto.]

## Aviso de segurança

Este projeto possui finalidade educacional e foi desenvolvido em um ambiente de testes controlado. Não deve ser utilizado para criptografar arquivos de terceiros ou dados sem autorização.
