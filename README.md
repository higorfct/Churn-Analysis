# Projeto-4-Análise de Churn

# 📊 Projeto: Análise de Evasão de Clientes (Churn Analysis)

## 📝 Introdução

Este projeto tem como objetivo identificar os principais fatores que levam à evasão de clientes (churn) em um banco com operações na Alemanha, na Espanha e na França, utilizando técnicas de machine learning e análise exploratória de dados com o intuito de formular políticas que aumentem a retenção dos clientes mais propensos a desistir dos serviços do banco e, dessa forma, minimizar o impacto financeiro gerado pelo churn.

---

## 📊 Dados

Foram utilizados dados contendo informações cadastrais e transacionais dos clientes, incluindo variáveis como **idade**, **saldo**, **salário estimado**, **produtos contratados** e se o cliente deixou ou não a instituição **(variável alvo: `Exited`)**.

### Etapas realizadas:
- Importação do dataset `Churn_treino.csv` com separador `;`
- Análise da distribuição da evasão por **localização geográfica**, **idade** e **gênero**
- Verificação e tratamento de valores faltantes
- Codificação de variáveis categóricas com `LabelEncoder`
- Padronização de variáveis numéricas com `StandardScaler`
- Balanceamento da base utilizando **SMOTE** para lidar com desbalanceamento da variável alvo

---

## 🤖 Modelagem Preditiva

Modelos aplicados:
- Rede Neural (Keras)
- Regressão Logística
- Random Forest
- Naive Bayes
- SVM
- AdaBoost
- XGBoost
- KNN
- LightGBM

Todos os modelos foram treinados com `train_test_split` e avaliados de acordo com as métricas **acurácia**, **precisão**, **recall** e **F1-score**.
---

## 🔍 Principais Insights

- Clientes mais velhos tendem a evadir com mais frequência.
- Clientes do país **“Germany”(Alemanha)** apresentaram maior taxa de evasão.
- Mulheres tiveram uma leve tendência maior à evasão em comparação às mulheres.
- A variável "Saldo" (balance) sozinha não é suficiente para prever churn, mas combinada com idade e número de produtos, aumenta seu poder preditivo.
- O modelo **XGBoost** foi o que apresentou melhor desempenho entre os algoritmos testados.

---

## 📈 Visualizações

- Gráfico de barras da evasão por localização (`Geography`)
- Histograma de idade com estratificação por churn
- Gráfico de barras do churn por gênero
- Matriz de confusão dos principais modelos
- Gráfico de comparação de métricas dos modelos
- Explicações locais com LIME para os resultados do modelo XGBoost

---

## 🛠️ Ferramentas Utilizadas

- **Python** – Linguagem principal  
- **Pandas** – Manipulação e análise de dados  
- **Seaborn / Matplotlib** – Visualização gráfica  
- **Scikit-learn** – Modelagem preditiva e métricas  
- **Keras / TensorFlow** – Construção de rede neural  
- **XGBoost / LightGBM** – Modelos de boosting  
- **LIME** – Explicabilidade dos modelos  
- **Imbalanced-learn (SMOTE)** – Balanceamento de classes  
- **Jupyter Notebook** – Ambiente de desenvolvimento  

---

## ✅ Resultados

- O modelo **LightGBM** apresentou as melhores métricas. No entanto, apesar de ter excedido os outros modelos a esse respeito, métricas como **F1-Score** e **recall** se mostraram bem baixas, sendo de **60%** e **52%**, respectivamente, mesmo com a utilização de SMOTE para balanceamento de classes. 
- Foi utilizada a técnica LIME de IA Explicável para desvendar os fatores que contribuem ou não para o churn de clientes.
- Os fatores que reduzem o risco de churn são: **idade(mais jovem = menor risco)**, **tempo como cliente** e **engajamento como membro ativo**.
- Os fatores que estão relacionados com o churn são: **alto salário**, **saldo elevado (maior poder de trocar de banco)**, **poucos produtos contratados** e **score abaixo da média(insegurança para o banco, talvez?**
---

## 💼  Impacto Financeiro do Modelo LightGBM

Ao definir:

- **Receita média por cliente:** R$ 100,00;
- **Métrica utilizada:** True Positives (TP) — clientes que realmente sairiam, mas foram corretamente identificados pelo modelo;
- **Hipótese:** todos os clientes identificados como TP são retidos com sucesso.

O modelo LightGBM, mesmo com algumas métricas com valor mais baixo do que o desejado (Recall e Precision), mostrou potencial de gerar uma **economia potencial de R$ 32.600,00**

## 🧠 Conclusões

O projeto mostrou como é possível usar **análise de dados e machine learning** para:

- Identificar perfis com maior propensão à evasão
- Aplicar técnicas de balanceamento de dados para melhorar a qualidade do modelo
- Avaliar diferentes algoritmos para encontrar o mais adequado ao problema
- Utilizar ferramentas como **LIME** para interpretar decisões de modelos complexos

---

## 🔄 Próximos Passos

- Implementar modelos em ambiente de produção com monitoramento contínuo
- Realizar tuning avançado de hiperparâmetros via **GridSearch**, **RandomSearch** ou **Bayesian Optimizer** para encontrar melhores métricas **F1-Score** e **Recall**, visto que quando tais métricas estão baixas, acaba-se deixando passar falsos positivos e negativos, o que pode representar altos prejuízos financeiros para a instituição.

---

🧑‍💻 **Autor e Contato**

**Higor Roberto Coutinho Caetano**  
**LinkedIn**: [https://www.linkedin.com/in/higor-caetano-049521136/](https://www.linkedin.com/in/higor-caetano-049521136/)  
**E-mail**: higorfct@gmail.com  
