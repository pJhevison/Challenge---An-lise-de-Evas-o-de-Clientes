# 📊 Análise de Evasão de Clientes (Churn) - Desafio Data Science

Este repositório contém a análise de dados completa para o desafio de Data Science focado em entender a evasão de clientes (Churn) em uma empresa fictícia de telecomunicações, a **Telecom X**.

---

## 🎯 Objetivo do Projeto

O objetivo principal deste projeto é realizar uma **análise exploratória de dados (EDA)** para identificar os principais fatores e perfis de clientes que levam ao cancelamento dos serviços.  
A partir dos insights gerados, foram propostas recomendações estratégicas para ajudar a empresa a desenvolver ações de **retenção mais eficazes**.

---

## 📊 Dataset

O conjunto de dados utilizado foi fornecido em formato JSON e contém informações sobre os clientes da Telecom X, incluindo:

- **Dados demográficos** (gênero, idade, etc.)
- **Detalhes do contrato** (tipo, tempo de contrato)
- **Serviços assinados** (internet, telefone, suporte técnico, etc.)
- **Informações financeiras** (gastos mensais e totais)

📁 O dataset bruto (`TelecomX_Data.json`) e o dicionário de dados (`TelecomX_dicionario.md`) estão disponíveis neste repositório.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **Python 3**
- `Pandas`: Manipulação e análise de dados
- `Seaborn` & `Matplotlib`: Criação de visualizações e gráficos
- **Google Colab / Jupyter Notebook**: Ambiente de desenvolvimento da análise

---

## 📁 Estrutura do Repositório

├── Challenge_Intercon_x_.ipynb # Notebook principal com a análise completa
├── TelecomX_Data.json # Arquivo de dados brutos
├── TelecomX_dicionario.md # Dicionário de dados do dataset
└── README.md # Este arquivo

---

## 📈 Metodologia

O projeto seguiu um fluxo de trabalho padrão de análise de dados (**ETL + EDA**):

### 🔹 Extração:
- Carregamento dos dados diretamente de uma **API** em formato JSON.

### 🔹 Transformação e Limpeza:
- Normalização da estrutura aninhada com `pandas.json_normalize`.
- Conversão de colunas como `Gasto_Total` de texto para numérico.
- Remoção de 224 registros com valores ausentes na coluna `Churn`.
- Padronização de categorias como `"No phone service"` para `"No"`.
- Criação da nova coluna `Contas_Diarias` (baseada no Gasto Mensal).
- Conversão de valores `"Yes"`/`"No"` para `1`/`0`.
- Renomeação das colunas para **português**.

### 🔹 Análise Exploratória de Dados (EDA):
- Visualização da **proporção de churn**.
- Análise cruzada com variáveis categóricas (Tipo de Contrato, Método de Pagamento, etc.).
- Boxplots comparativos de `Tempo_de_Contrato` e `Gasto_Mensal`.
- **Matriz de correlação** entre variáveis numéricas.

---

## 💡 Principais Conclusões e Insights

- 📌 **Contrato "Mês a Mês"**: Associado à maior taxa de churn.
- 📉 **Baixo tempo de contrato**: Clientes nos primeiros meses são mais propensos a cancelar.
- 💰 **Gasto Mensal elevado**: Leva a maior insatisfação e cancelamento.
- 💳 **Cheque Eletrônico**: Método de pagamento com maior evasão.
- 🔒 **Falta de serviços como Suporte Técnico e Segurança Online** também aumenta o risco de churn.

---

## 🧠 Recomendações Estratégicas

- 🎯 **Migrar clientes do plano "Mês a Mês"** para contratos mais longos com benefícios.
- 📦 **Programa de boas-vindas** para os primeiros 3 meses do cliente.
- 💳 **Incentivar o uso de pagamentos automáticos** com bônus ou descontos.
- 🔧 **Oferecer serviços de valor agregado** para clientes de risco (Ex: Suporte Técnico e Segurança Online).

---

## 🚀 Como Executar o Projeto

### Clone o repositório:

```bash
git clone https://github.com/pJhevison/Challenge---An-lise-de-Evas-o-de-Clientes.git
✍️ Autor
Pedro Jhevison Menezes
LinkedIn | GitHub
