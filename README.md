# 📊 Prevendo Churn – Telecom X (Parte 2)

Este projeto foi desenvolvido como parte do desafio **Telecom X – Parte 2: Prevendo Churn**, cujo objetivo é criar modelos de *Machine Learning* capazes de prever quais clientes têm maior probabilidade de cancelar seus serviços (*churn*).

---

## 🎯 Objetivo

Construir um pipeline preditivo robusto para:
- Realizar pré-processamento de dados (limpeza, normalização, codificação de variáveis).
- Analisar correlações e selecionar variáveis relevantes.
- Balancear classes para lidar com desbalanceamento no churn.
- Treinar e avaliar diferentes modelos de classificação.
- Extrair insights estratégicos para retenção de clientes.

---

## 📂 Estrutura da Pasta

```
📁 projeto-churn-telecomx
│-- 📄 Relatorio_TelecomX_2.docx      # Relatório final com resultados e conclusões
│-- 📄 README.md                      # Este arquivo
│-- 📄 dados_normalizados_TELECOMX_PT.csv  # Base de dados tratada
│-- 📄 Challenge_X2.ipynb             # Notebook com código, análises e modelos
```

---

## 🛠 Tecnologias e Bibliotecas Utilizadas

- **Python** 3.x
- **Pandas** e **NumPy** – Manipulação e análise de dados
- **Matplotlib** e **Seaborn** – Visualização de dados
- **SciPy** – Estatísticas
- **Scikit-learn** – Modelos de machine learning e pré-processamento
- **Imbalanced-learn (SMOTE)** – Balanceamento de classes
- **Statsmodels** – Modelos estatísticos e análise de variáveis

---

## 📊 Etapas do Projeto

1. **Carregamento da Base de Dados**
   - Utilização de `dados_normalizados_TELECOMX_PT.csv` (resultado do Challenge 1 com dados tratados).

2. **Pré-processamento**
   - Conversão de variáveis categóricas (`genero`) para valores numéricos.
   - Padronização de variáveis numéricas pelo método **Z-score**.
   - Codificação *One-Hot Encoding* para variáveis categóricas (`tipo_internet`, `tipo_contrato`, `forma_pagamento`).
   - Remoção de variáveis redundantes.

3. **Análise de Correlação**
   - Correlação de Spearman com a variável alvo `cancelou`.
   - Identificação de fatores de retenção e de risco para churn.

4. **Divisão de Dados**
   - Separação treino/teste (70%/30%) com estratificação para manter proporção das classes.

5. **Balanceamento**
   - Aplicação de **SMOTE** somente no conjunto de treino.

6. **Treinamento e Avaliação de Modelos**
   - **Árvore de Decisão** (ajustes de `max_depth` para reduzir overfitting).
   - **K-Nearest Neighbors (KNN)**.
   - **Regressão Logística** (interpretação de coeficientes).
   - Comparação das métricas: *accuracy*, *precision*, *recall*, *f1-score*.

7. **Interpretação e Insights**
   - Fatores que mais influenciam o cancelamento e a retenção.
   - Recomendações estratégicas para retenção de clientes.

---

## 📈 Principais Resultados

- **Árvore de Decisão (max_depth=3)**: Recall de 86% para classe "cancelou" – indicado quando a prioridade é identificar o máximo possível de cancelamentos.
- **KNN**: Recall de 72% para cancelamentos – desempenho intermediário.
- **Regressão Logística**: Melhor equilíbrio entre precisão e recall, além de alta interpretabilidade.

---

---

## 📌 Autor
**Mateu Xauan** – Analista de Machine Learning Júnior  
Projeto desenvolvido para o desafio **Telecom X – Parte 2**.
