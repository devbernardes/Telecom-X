# Análise de Evasão de Clientes (Churn) - Telecom X

## 📄 Descrição do Projeto

Este projeto consiste em uma análise exploratória de dados sobre a evasão de clientes (Churn) de uma empresa fictícia do setor de telecomunicações, a Telecom X. O objetivo principal é identificar os principais fatores que influenciam a decisão de um cliente cancelar seu serviço, a fim de subsidiar a criação de estratégias de retenção mais eficazes.

## 🎯 Objetivo

O problema de negócio a ser resolvido é a alta taxa de evasão de clientes, que gera custos elevados de aquisição e impacta a receita da empresa. Esta análise busca responder às seguintes perguntas:
* Qual é o perfil demográfico dos clientes que evadem?
* Quais serviços ou tipos de contrato estão mais associados ao Churn?
* Como fatores financeiros, como a cobrança mensal, se relacionam com a evasão?

## 📂 Fonte dos Dados

Os dados foram obtidos de uma API em formato JSON, disponibilizada para o desafio. O dataset contém informações sobre 7.043 clientes, incluindo dados demográficos, serviços contratados, informações de contrato e o status de evasão.

## 🛠️ Ferramentas e Bibliotecas Utilizadas

* **Linguagem:** Python
* **Bibliotecas Principais:**
    * `pandas` para manipulação e tratamento dos dados.
    * `matplotlib` e `seaborn` para visualização de dados.
    * `requests` para carregamento dos dados via API.

## ⚙️ Metodologia

O projeto seguiu um fluxo de trabalho padrão de Data Science:

1.  **Coleta e Carregamento dos Dados:** Importação dos dados diretamente da fonte JSON, tratando a estrutura aninhada com `pandas.json_normalize`.
2.  **Limpeza e Pré-processamento:**
    * Conversão de tipos de dados (ex: coluna de cobrança total para numérica).
    * Tratamento de valores ausentes.
    * Verificação de dados duplicados.
3.  **Engenharia de Atributos:** Criação da coluna `Cobranca_Diaria` para normalizar a análise de custos.
4.  **Transformação de Dados:**
    * Renomeação das colunas para português para maior clareza.
    * Codificação de variáveis categóricas (binárias e multi-categoria via One-Hot Encoding) para preparar os dados para análises estatísticas e modelagem.
5.  **Análise Exploratória de Dados (AED):**
    * Análise descritiva para extrair estatísticas centrais.
    * Análise de correlação para identificar a relação entre as variáveis e a evasão.
    * Visualizações (histogramas, boxplots) para entender a distribuição dos dados e comparar os perfis de clientes que evadiram e que permaneceram.

## 💡 Principais Insights

A análise revelou um perfil claro do cliente com alta propensão à evasão:
* **Contrato Mensal:** É o fator de risco mais significativo. A flexibilidade deste tipo de contrato facilita o cancelamento.
* **Clientes Novos:** A evasão é muito mais concentrada em clientes com poucos meses de contrato (média de 18 meses para quem sai vs. 38 para quem fica).
* **Cobrança Mensal Elevada:** Clientes com faturas mensais mais altas (média de R$74) tendem a sair mais do que aqueles com faturas mais baixas (média de R$61).

## 🚀 Recomendações Estratégicas

Com base nos insights, as seguintes ações são recomendadas:
1.  **Incentivar Contratos de Longo Prazo:** Criar campanhas e descontos agressivos para migrar clientes do plano mensal para planos anuais ou bianuais.
2.  **Programas de Retenção para Novos Clientes:** Focar esforços de retenção nos primeiros 6 meses de vida do cliente, oferecendo suporte proativo e benefícios de boas-vindas.
3.  **Desenvolver um Modelo Preditivo:** Utilizar os dados tratados para construir um modelo de Machine Learning que identifique clientes em risco de evasão, permitindo ações de retenção personalizadas e proativas.

## ✍️ Autor(a)

* **[Gabriel Santana Bernardes]**
* **LinkedIn:** [www.linkedin.com/in/gabriesbernardes]
* **Email:** [Gabriel.original2001@gmail.com]
