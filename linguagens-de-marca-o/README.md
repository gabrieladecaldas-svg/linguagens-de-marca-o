# Linguagens de Marcação - Exercícios Práticos de XML

Este repositório contém a resolução dos exercícios práticos de **Sintaxe e Validação XML**, referentes à Unidade Curricular de **Linguagens de Marcação**.

## 📌 Objetivos da Atividade
* Compreender os fundamentos e regras sintáticas da linguagem XML.
* Identificar e corrigir erros de sintaxe em documentos XML (tags não fechadas, atributos sem aspas, caracteres especiais não escapados, nomes de elementos inválidos e erros de aninhamento).
* Garantir que todos os documentos estejam **bem-formados** (*Well-Formed XML*) de acordo com as especificações do W3C.

---

## 🛠️ Resumo das Correções Efetuadas

### 🔹 Exercício 1: Cadastro de Livro (`exercicio1.xml`)
* **Erro Identificado:** A tag `<titulo>` foi aberta, mas não foi fechada antes do elemento seguinte.
* **Correção:** Adicionado o fechamento explicito `</titulo>`.


### 🔹 Exercício 2: Cadastro de Aluno (`exercicio2.xml`)
* **Erros Identificados:** 
  1. O atributo `matricula=202501` estava sem aspas.
  2. A tag `<idade=20></idade>` tentou atribuir valor no nome da tag com `=`.
* **Correção:** Adicionadas aspas ao atributo (`matricula="202501"`) e corrigida a estrutura do elemento para `<idade>20</idade>`.

### 🔹 Exercício 3: Empresa (`exercicio3.xml`)
* **Erros Identificados:** 
  1. Declaração XML malformada (`version=1.0` sem aspas e sem fechamento `?>`).
  2. Uso do caractere especial `&` no texto sem o devido escape.
* **Correção:** Ajustada a instrução de processamento `<?xml version="1.0" encoding="UTF-8"?>` e substituído `&` por `&amp;`.

### 🔹 Exercício 4: Pedido de Venda (`exercicio4.xml`)
* **Erro Identificado:** Quebra da regra de aninhamento LIFO (Last In, First Out). A tag `<itens>` foi aberta dentro de `<cliente>`, mas `</cliente>` foi fechada antes de `</itens>`.
* **Correção:** Separadas as estruturas de `<cliente>` e `<itens>` como elementos irmãos dentro do elemento raiz `<pedido>`.

### 🔹 Exercício 5: Cadastro de Produtos (`exercicio5.xml`)
* **Erros Identificados:** 
  1. A tag `<nome produto>` continha espaço em branco no nome do elemento.
  2. A tag `<1preco>` começava com um dígito numérico, o que é proibido em XML.
* **Correção:** Renomeadas as tags para `<nome>` e `<preco>`, e encapsuladas dentro do bloco `<produto>`.

### 🔹 Exercício 6: Sistema Escolar - Desafio (`exercicio6.xml`)
* **Erros Identificados:** 
  1. Aspas misturadas na declaração (`version='1.0"`) e no atributo (`matricula='202501"`).
  2. Atributo `curso=Informática` sem aspas.
  3. Caractere `&` não escapado no nome ("Lucas & Ana").
  4. Tag `<disciplina>Banco de Dados` sem fechamento.
* **Correção:** Padronização de todas as aspas duplas, substituição do `&` por `&amp;` e inserção da tag de fechamento `</disciplina>`.

---

## 📁 Estrutura do Repositório

```text
.
├── exercicio1.xml   # Cadastro de Livro
├── exercicio2.xml   # Cadastro de Aluno
├── exercicio3.xml   # Cadastro de Empresa
├── exercicio4.xml   # Pedido de Venda
├── exercicio5.xml   # Cadastro de Produtos
├── exercicio6.xml   # Sistema Escolar (Desafio)
└── README.md        # Documentação da atividade