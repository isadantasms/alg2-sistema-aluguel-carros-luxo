# 🚗 Sistema de Aluguel de Carros de Luxo (C Puro)

[![C Language](https://img.shields.io/badge/Language-C99-00599C?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C99)
[![University](https://img.shields.io/badge/UFU-FACOM-003366?style=for-the-badge)](https://facom.ufu.br/)
[![Course](https://img.shields.io/badge/BSI-Algoritmos_&_Prog_II-orange?style=for-the-badge)](https://facom.ufu.br/)

Sistema desenvolvido em **Linguagem C (C99)** para gerenciamento e controle operacional de uma locadora de veículos de luxo, com persistência binária, manipulação dinâmica de memória e geração de relatórios formatados em arquivo de texto.

Trabalho prático da disciplina **Algoritmos e Programação II (FACOM32201)** do curso de **Sistemas de Informação** da **Universidade Federal de Uberlândia (UFU)**.

---

## 📌 Funcionalidades Principais

* **👤 Módulo de Clientes:** Cadastro, consulta, listagem e exclusão de clientes com validação de CPF único, endereço e telefone.
* **🏎️ Módulo de Veículos:** Registro de modelos de luxo, placa única, ano, categoria e valor da diária.
* **📑 Módulo de Aluguéis:** Associação dinâmica entre cliente e veículo, controle de datas, cálculo automático de valor total e verificação de disponibilidade.
* **📊 Geração de Relatórios (Texto):** Exportação de relatórios analíticos formatados:
  * Relatório consolidado de aluguéis por período;
  * Relatório de disponibilidade da frota;
  * Relatório financeiro de faturamento.
* **💾 Persistência em Arquivos Binários:** Leitura e gravação serializada em arquivos `.bin` (`clientes.bin`, `carros.bin`, `alugueis.bin`).
* **🧠 Gerenciamento Dinâmico de Memória:** Alocação e redimensionamento dinâmico de vetores em tempo de execução via `malloc` e `realloc`.

---

## 🏛️ Arquitetura Modular

O projeto foi dividido em módulos com separação estrita entre cabeçalhos (`.h`) e implementações (`.c`):

```text
├── modelos.h        # Definição das structs centrais (Cliente, Carro, Aluguel)
├── cliente.c/.h     # Lógica e validação das operações de clientes
├── carro.c/.h       # Lógica e controle de status da frota de veículos
├── aluguel.c/.h     # Regras de negócio, cálculo de diárias e reservas
├── relatorios.c/.h  # Exportação de relatórios tabulares em arquivo de texto
├── util.c/.h        # Funções utilitárias (tratamento de strings, limpeza de buffer)
├── main.c           # Menu interativo e orquestração do sistema
├── alugueis.bin     # Arquivo binário de dados pré-carregados
├── carros.bin       # Arquivo binário de veículos
└── clientes.bin     # Arquivo binário de clientes
```

---

## 🚀 Como Compilar e Executar

### Pré-requisitos
* Compilador GCC instalado (`gcc --version`).

### Compilação
Execute o comando abaixo no terminal dentro do diretório do projeto:

```bash
gcc -Wall -Wextra -std=c99 main.c cliente.c carro.c aluguel.c relatorios.c util.c -o sistema_aluguel
```

### Execução
```bash
./sistema_aluguel
```

> **Nota:** Certifique-se de executar o binário dentro do mesmo diretório dos arquivos `.bin` para carregar a base de dados pré-preenchida.

---

## 👥 Equipe do Projeto (UFU)

* **Isabela Dantas de Moraes**
* **Isabela de Sousa Faria Pereira Rocha**
* **Celina Vieira Silva**
* **Gabriel Manzini Toledo**
* **Kauã Magalhães dos Santos**

* **Docente Responsável:** Prof. Dr. Thiago Pirola Ribeiro (FACOM/UFU)
