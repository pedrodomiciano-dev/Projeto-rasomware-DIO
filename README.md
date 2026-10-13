# Laboratório de Criptografia de Arquivos com Python

## Sobre o projeto

Este projeto é um laboratório educacional de cibersegurança desenvolvido em Python para demonstrar o funcionamento da criptografia e descriptografia de arquivos utilizando o algoritmo AES no modo CTR.

O experimento utiliza a biblioteca `pyaes` e um arquivo de texto descartável para observar como o conteúdo original é transformado em dados criptografados e posteriormente recuperado.

## Objetivos

- Compreender o funcionamento básico da criptografia simétrica.
- Utilizar Python para manipular arquivos em modo binário.
- Aplicar o algoritmo AES no modo CTR.
- Observar as alterações nos arquivos durante a criptografia e a descriptografia.
- Praticar o uso do Kali Linux e a documentação de experimentos técnicos.

## Tecnologias utilizadas

- Python 3
- Kali Linux
- Biblioteca `pyaes`
- AES-128 no modo CTR
- Git e GitHub

## Estrutura do projeto

```text
projeto-aes/
├── encrypter.py
├── decrypter.py
├── teste.txt
├── README.md
└── evidencias/
```

## Funcionamento

### 1. Criptografia

O script `encrypter.py`:

1. Abre `teste.txt` em modo binário.
2. Lê o conteúdo do arquivo.
3. Remove o arquivo original.
4. Criptografa os dados utilizando AES-CTR.
5. Grava o resultado em `teste.txt.ransomwaretroll`.

### 2. Descriptografia

O script `decrypter.py`:

1. Abre o arquivo criptografado.
2. Lê os dados em modo binário.
3. Utiliza a mesma chave para recuperar o conteúdo.
4. Remove o arquivo criptografado.
5. Cria novamente `teste.txt` com os dados recuperados.

## Como executar

### Pré-requisitos

- Python 3 instalado.
- Biblioteca `pyaes`.
- Terminal Linux.

### Preparação do ambiente

Crie e ative um ambiente virtual:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Instale a dependência:

```bash
python -m pip install pyaes
```

### Executando o experimento

Com um arquivo descartável `teste.txt` contendo texto de exemplo, execute:

```bash
python encrypter.py
```

Confira o arquivo produzido:

```bash
ls -l teste.txt*
```

Para observar os bytes criptografados:

```bash
xxd teste.txt.ransomwaretroll
```

Para recuperar o conteúdo original:

```bash
python decrypter.py
```

Confira o resultado:

```bash
cat teste.txt
```

## Resultados observados

Durante o teste, o conteúdo legível do arquivo foi transformado em dados não legíveis diretamente após a execução do criptografador.

O arquivo criptografado recebeu a extensão `.ransomwaretroll`. Após executar o descriptografador, o arquivo original foi recriado e o texto pôde ser lido novamente.

As capturas de tela dos testes estão disponíveis na pasta `evidencias/`.

## Considerações de segurança

Este projeto é exclusivamente educacional.

A chave está definida diretamente no código, e o modo CTR não oferece autenticação ou garantia de integridade dos dados por si só. O exemplo não deve ser considerado uma implementação segura para proteger arquivos reais.

Os scripts removem arquivos durante a execução. Por isso, os testes devem ser realizados somente com arquivos descartáveis e cópias de segurança.

## Aprendizados

- Manipulação de arquivos com Python.
- Leitura e gravação em modo binário.
- Uso de bibliotecas criptográficas.
- Diferença entre dados legíveis e dados criptografados.
- Organização e documentação de um projeto técnico.
- Registro de evidências de um experimento de laboratório.
