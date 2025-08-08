# 📊 Projeto de Análise de Churn em Telecom

Este projeto tem como objetivo analisar e construir um modelo preditivo para identificar clientes com maior probabilidade de **cancelar serviços (churn)** em uma empresa de telecomunicações. Todo o processo foi desenvolvido em um Jupyter Notebook, seguindo uma abordagem passo a passo — da exploração de dados à preparação para Machine Learning.

---

## 📌 1. Visão Geral do Projeto

O foco principal é a variável **Churn** (renomeada para `Cancelou`), que indica se um cliente desistiu dos serviços da empresa. O projeto realiza as seguintes etapas:

- Limpeza e inspeção inicial dos dados.
- Tradução e padronização de variáveis.
- Transformações e normalizações necessárias.
- Preparação dos dados para modelagem preditiva.

---

## 🛠️ 2. Tecnologias e Bibliotecas Utilizadas

O projeto foi desenvolvido em **Python**, utilizando bibliotecas do ecossistema de Ciência de Dados:

- **pandas**: Manipulação e análise de dados.
- **numpy**: Operações matemáticas e vetoriais.
- **matplotlib.pyplot** & **seaborn**: Visualização de dados.
- **scipy** & **statsmodels**: Testes estatísticos e análise inferencial.
- **scikit-learn (sklearn)**:
  - `preprocessing`: Normalização (MinMaxScaler, StandardScaler), codificação (OneHotEncoder).
  - `linear_model`: Regressão logística.
  - `model_selection`: Separação em treino/teste (train_test_split).
  - `compose`: Uso de ColumnTransformer para aplicar diferentes transformações nas colunas.

---

## 🧾 3. Estrutura dos Dados

- Arquivo utilizado: `dados_normalizados.csv`
- Total de registros: **7.267**
- Total de colunas: **24**
- Tipos de dados: booleanos, inteiros, floats e objetos.

### Principais colunas (com nomes traduzidos):
| Nome Original     | Nome Traduzido     |
|-------------------|--------------------|
| `customerID`      | `ID_Cliente`       |
| `Churn`           | `Cancelou`         |
| `gender`          | `Genero`           |
| `SeniorCitizen`   | `Idoso`            |
| `tenure`          | `Meses_de_Contrato`|
| `MonthlyCharges`  | `Valor_Mensal`     |

---

## 🧪 4. Metodologia

O notebook segue a seguinte estrutura:

### 1. Carregamento e Inspeção dos Dados
- Leitura do arquivo `.csv` com `pandas`
- Análise da estrutura do DataFrame com `df.info()`

### 2. Pré-processamento
- **Tradução de Colunas**: Renomeadas para o português para facilitar a leitura.
- **Conversão de Variáveis Categóricas**: Ex: `Genero` transformado em valor booleano.
- **Normalização/Padronização**:
  - MinMaxScaler e StandardScaler aplicados nas colunas numéricas:
    - `Meses_de_Contrato`
    - `Valor_Mensal`
    - `Qtd_Servicos`
    - `Total_Servicos`
  - StandardScaler foi a última transformação utilizada.

### 3. Preparação para o Modelo
- **Separação de variáveis**:
  - `Cancelou` como variável alvo (**Y**)
  - Remoção de `ID_Cliente` e `Cancelou` das features (**X**)
- **Codificação One-Hot**:
  - Aplicada às colunas categóricas como `Tipo_Internet`, `Tipo_Contrato`, `Metodo_Pagamento`, etc.
  - Utilizado `OneHotEncoder` em conjunto com `ColumnTransformer`.

---

## 📂 Organização do Projeto

```
├── dados_normalizados.csv
├── analise_churn_telecom.ipynb
└── README.md
```

---

## ✅ Status do Projeto

✔️ Análise e pré-processamento concluídos  
🧠 Pronto para a construção e avaliação de modelos de Machine Learning
