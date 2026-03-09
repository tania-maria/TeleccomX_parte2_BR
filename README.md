# 📊 Previsão de Churn - Telecom X

## 💡 Sobre o Projeto
Este projeto tem como objetivo **prever quais clientes da Telecom X têm maior probabilidade de cancelar seus serviços (churn)**. Antecipar a evasão de clientes permite à empresa planejar ações de retenção, melhorar a experiência do cliente e reduzir perdas financeiras.

Foram utilizados dados de clientes que incluem informações demográficas, tipo de serviço contratado, histórico de pagamentos e uso de serviços adicionais. Técnicas de **Machine Learning** foram aplicadas para análise preditiva e interpretação dos fatores que influenciam a evasão.

---

## 🧾 Etapas do Projeto

### 1️⃣ Extração e Limpeza dos Dados
- Carregamento do arquivo CSV previamente tratado.  
- Remoção de colunas irrelevantes, como `customerID`, que não contribuem para a previsão.

### 2️⃣ Pré-processamento
- Transformação de variáveis categóricas em numéricas com **one-hot encoding**.  
- Normalização dos dados quando necessário para modelos sensíveis à escala (ex: Regressão Logística, KNN).  
- Balanceamento de classes usando **SMOTE**, devido à proporção desbalanceada (aprox. 26% de churn).

### 3️⃣ Análise Exploratória de Dados (EDA)
- Visualização da **distribuição de churn**.  
- Matriz de correlação para identificar relações entre variáveis.  
- Análises direcionadas com **boxplots** e gráficos de dispersão, observando padrões como:  
  - `customer_tenure x Churn`  
  - `account_Charges_Total x Churn`

### 4️⃣ Criação de Modelos Preditivos
- **Regressão Logística**: modelo linear que permite interpretar a influência das variáveis.  
- **Random Forest**: modelo baseado em árvores, robusto a dados não normalizados e capaz de fornecer a importância das variáveis.

### 5️⃣ Avaliação dos Modelos
- Métricas utilizadas:  
  - **Acurácia**  
  - **Precisão (Precision)**  
  - **Recall**  
  - **F1-Score**  
  - **Matriz de Confusão**
- Comparação do desempenho entre os modelos e análise de possíveis **overfitting/underfitting**.

### 6️⃣ Importância das Variáveis
- Identificação das variáveis mais relevantes para a previsão de churn:  
  - Tempo de contrato (`customer_tenure`)  
  - Total gasto (`account_Charges_Total`)  
  - Serviços adicionais contratados (Streaming TV/Movies, Suporte Técnico, etc.)

### 7️⃣ Conclusão
- O projeto permitiu compreender os fatores que influenciam a evasão de clientes.  
- Insights obtidos podem ser utilizados para **estratégias de retenção e tomada de decisão** da empresa.

---

## 📂 Estrutura do Repositório

-------------

## 🛠 Tecnologias e Bibliotecas
- **Python 3**  
- **Pandas, NumPy** – manipulação e análise de dados  
- **Seaborn, Matplotlib** – visualização de dados  
- **Scikit-learn** – modelos de Machine Learning (Logistic Regression, Random Forest, train_test_split, metrics)  
- **Imbalanced-learn (SMOTE)** – balanceamento de classes  

---

## 📈 Resultados
- Acurácia aproximada dos modelos:  
  - **Regressão Logística**: 80%  
  - **Random Forest**: 78%  
- Modelos identificaram que clientes com **contratos de curto prazo e maior gasto total** têm maior probabilidade de churn.  

---

## ⚡ Próximos Passos
- Testar outros modelos, como **XGBoost** ou **SVM**, para melhorar desempenho.  
- Implementar uma **pipeline completa** para atualização automática com novos dados.  
- Criar dashboards para visualização interativa dos insights obtidos.





