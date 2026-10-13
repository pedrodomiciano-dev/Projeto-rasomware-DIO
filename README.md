
# Projeto DIO: Criptografia AES

## Descrição

Projeto desenvolvido em Python para estudar a criptografia e a descriptografia de arquivos utilizando a biblioteca `pyaes` e o algoritmo AES no modo CTR.

O objetivo é compreender a manipulação de arquivos binários, o uso de bibliotecas externas e o funcionamento básico de um processo de criptografia e recuperação de dados.

## Tecnologias

- Python 3
- Biblioteca `pyaes`
- Kali Linux
- Git e GitHub

## Arquivos

- `encrypter.py`: criptografa o arquivo de teste.
- `decrypter.py`: descriptografa o arquivo e restaura seu conteúdo.
- `teste.txt`: arquivo utilizado durante os testes.
- `.gitignore`: define arquivos que devem ser ignorados pelo Git.

## Execução

Instale a dependência `pyaes` no ambiente Python utilizado:

```bash
python -m pip install pyaes
```

Execute primeiro o script de criptografia:

```bash
python encrypter.py
```

Depois, execute o script de descriptografia:

```bash
python decrypter.py
```

## Conceitos estudados

- Leitura e escrita de arquivos em modo binário.
- Manipulação de arquivos com Python.
- Uso de bibliotecas externas.
- Criptografia e descriptografia AES-CTR.
- Controle de versão com Git.

## Observações de segurança

Este projeto é exclusivamente educacional. Os scripts removem arquivos durante o processo e não implementam mecanismos robustos de recuperação em caso de falha.

A chave é fixa e está definida diretamente no código. O modo CTR não fornece autenticação ou integridade dos dados por si só.

Utilize somente arquivos descartáveis em um ambiente controlado. Não utilize este projeto para proteger dados reais ou em sistemas de terceiros.
