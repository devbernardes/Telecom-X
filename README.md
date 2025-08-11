# Análise de Evasão de Clientes (Churn) - Telecom X (1 e 2)

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
    * `scikit-learn` para modelagem preditiva e avaliação de modelos.
    * `requests` para carregamento dos dados via API.

## ⚙️ Metodologia

O projeto seguiu um fluxo de trabalho padrão de Data Science:

1. **Coleta e Carregamento dos Dados:** Importação dos dados diretamente da fonte JSON, tratando a estrutura aninhada com `pandas.json_normalize`.
2. **Limpeza e Pré-processamento:**
    * Conversão de tipos de dados (ex: coluna de cobrança total para numérica).
    * Tratamento de valores ausentes.
    * Verificação de dados duplicados.
3. **Engenharia de Atributos:** Criação da coluna `Cobranca_Diaria` para normalizar a análise de custos.
4. **Transformação de Dados:**
    * Renomeação das colunas para português para maior clareza.
    * Codificação de variáveis categóricas (binárias e multi-categoria via One-Hot Encoding) para preparar os dados para análises estatísticas e modelagem.
5. **Análise Exploratória de Dados (AED):**
    * Análise descritiva para extrair estatísticas centrais.
    * Análise de correlação para identificar a relação entre as variáveis e a evasão.
    * Visualizações (histogramas, boxplots) para entender a distribuição dos dados e comparar os perfis de clientes que evadiram e que permaneceram.

---

## 💡 Principais Insights da Versão 2

A **versão 2** do projeto introduziu novos **modelos preditivos** e **análises de variáveis**:

* **Regressão Logística**: A análise dos **coeficientes** indicou que variáveis como **Meses de Contrato** e **Total Gasto** são as mais influentes na previsão da evasão.
* **Random Forest**: As variáveis **Serviço de Internet (Fiber optic)** e **Método de Pagamento (Electronic check)** mostraram-se altamente impactantes na **importância das variáveis**.
* **KNN**: A proximidade entre os clientes foi analisada e revelou que clientes com **contratos mensais** e **alto gasto** são mais propensos à evasão.
* **SVM**: A análise da **fronteira de decisão** entre os clientes que evadiram e os que permaneceram indicou que **fatores financeiros e de contrato** são determinantes.

## 🚀 Recomendações Estratégicas

Com base nos insights da versão 2, as seguintes ações são recomendadas:

1. **Incentivar Contratos de Longo Prazo**: Criar campanhas e descontos agressivos para migrar clientes do plano mensal para planos anuais ou bianuais.
2. **Programas de Retenção para Novos Clientes**: Focar esforços de retenção nos primeiros 6 meses de vida do cliente, oferecendo suporte proativo e benefícios de boas-vindas.
3. **Desenvolver um Modelo Preditivo**: Utilizar os dados tratados para construir um modelo de **Machine Learning** que identifique clientes em risco de evasão, permitindo ações de retenção personalizadas e proativas.

## 📊 Desempenho dos Modelos de Machine Learning

A seguir, os **resultados de desempenho** dos modelos de machine learning aplicados na versão 2:

| Modelo            | Acurácia | Precisão | Recall  | F1-score |
|-------------------|----------|----------|---------|----------|
| **Regressão Logística** | 79.46%   | 64.71%   | 50%     | 56.5%    |
| **Random Forest**     | 80.67%   | 62.5%    | 46.2%   | 53.96%   |
| **KNN**               | 78.5%    | 61.1%    | 52.3%   | 56.2%    |
| **SVM**               | 79.0%    | 62.0%    | 49.5%   | 55.7%    |

### **Análise Comparativa dos Modelos:**
- **Random Forest** obteve o melhor desempenho em **acurácia**, mas apresentou um **recall** relativamente baixo, indicando que há espaço para melhorar na identificação de clientes que irão evadir.
- **Regressão Logística** teve um desempenho mais equilibrado entre **precisão** e **recall**, porém o **recall** de 50% sugere a necessidade de ajustes para identificar melhor os clientes que irão evadir.
- **KNN** teve um bom **recall** (52.3%) e F1-score (56.2%), indicando sua capacidade de capturar clientes propensos à evasão.
- **SVM** teve um desempenho moderado, mas não conseguiu superar os outros modelos em termos de **recall**.

---

## ✍️ Autor(a)

* **[Gabriel Santana Bernardes]**
* **LinkedIn:** [www.linkedin.com/in/gabriesbernardes]
* **Email:** [Gabriel.original2001@gmail.com]
