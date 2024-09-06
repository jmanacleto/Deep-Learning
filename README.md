# Documentação do Projeto: Previsão de Doenças Cardíacas utilizando Deep Learning

## Objetivo

O objetivo principal deste projeto é construir modelo de Deep Learning que possam prever atraves de uma rede neural probabilidade de uma pessoa ter uma doença cardíaca, com base em características  clínicas e comportamentais. Além disso, busca-se identificar os principais fatores de risco associados à doença, através de técnicas de exploração de dados e análise estatística.

## Descrição do Conjunto de Dados

O dataset utilizado no projeto contém as seguintes colunas:

- **Age**: Idade do paciente.
- **Gender**: Gênero do paciente (0 para feminino e 1 para masculino).
- **Cholesterol**: Nível de colesterol.
- **Blood Pressure**: Pressão arterial.
- **Heart Rate**: Frequência cardíaca.
- **Smoking**: Status de tabagismo (0 para nunca, 1 para atual, 2 para ex-fumante).
- **Alcohol Intake**: Consumo de álcool (0 para moderado, 1 para pesado).
- **Exercise Hours**: Horas de exercício por semana.
- **Family History**: Histórico familiar de doenças cardíacas.
- **Diabetes**: Presença de diabetes.
- **Obesity**: Índice de obesidade.
- **Stress Level**: Nível de estresse.
- **Blood Sugar**: Nível de açúcar no sangue.
- **Exercise Induced Angina**: Angina induzida por exercício.
- **Chest Pain Type**: Tipo de dor no peito.
- **Heart Disease**: Indicador de presença de doença cardíaca (variável alvo).

## Metodologia

### 1. Análise Exploratória de Dados (EDA)

Inicialmente, foi realizada uma análise exploratória dos dados para entender a distribuição das variáveis, identificar outliers e tratar valores ausentes. A EDA incluiu a verificação de outliers nas colunas **Age**, **Cholesterol**, **Blood Pressure**, **Heart Rate** e **Blood Sugar** através de gráficos de caixa (boxplots) e a criação de gráficos de curva normal para as mesmas colunas.

### 2. Tratamento de Valores Ausentes

Os valores ausentes nas colunas foram tratados de duas formas principais:
- Para as colunas numéricas (**Heart Rate**, **Blood Pressure**), os valores ausentes foram preenchidos com a média.
- Para as colunas categóricas (**Smoking**), os valores ausentes foram preenchidos com a moda (valor mais frequente).

### 3. Transformação e Normalização dos Dados

Algumas variáveis categóricas foram binarizadas para facilitar a modelagem, como a coluna **Alcohol Intake**, onde "Heavy" foi codificado como 1 e "Moderate" como 0. As colunas numéricas foram normalizadas utilizando `StandardScaler` para garantir que todas as variáveis tivessem a mesma escala.

### 4. Modelagem Preditiva

Foram utilizados diversos modelos de Machine Learning para prever a presença de doenças cardíacas, incluindo:
- **Regressão Logística**: Utilizada para prever a variável alvo baseada nas características selecionadas. O modelo foi treinado e avaliado utilizando validação cruzada.
- **Random Forest**: Utilizado para avaliar a importância das variáveis na predição de doenças cardíacas.

### 5. Avaliação e Validação

Os modelos foram avaliados com métricas como acurácia e validação cruzada. A acurácia do modelo de Regressão Logística foi calculada para o conjunto de teste, assim como a acurácia média através de validação cruzada.

## Resultados

Os resultados indicam que variáveis como **Blood Pressure**, **Cholesterol**, e **Age** têm um impacto significativo na predição de doenças cardíacas. O modelo de Regressão Logística apresentou boa performance, sendo uma ferramenta útil para a detecção precoce de doenças cardíacas.

## Conclusão

Este projeto demonstra a aplicação de técnicas de Machine Learning para a predição de doenças cardíacas, oferecendo insights sobre os principais fatores de risco. Os modelos desenvolvidos podem ser utilizados em aplicações clínicas para auxiliar na tomada de decisões e melhorar a saúde cardiovascular dos pacientes.

## Futuras Melhorias

- **Aprimoramento dos Modelos**: Testar outros modelos de classificação como SVM e redes neurais.
- **Aumento do Dataset**: Incorporar mais dados para melhorar a robustez do modelo.
- **Análise de Feature Engineering**: Explorar novas formas de engenharia de características para melhorar a performance dos modelos.

## Referências

- [Kaggle - Heart Disease Prediction Dataset](https://www.kaggle.com/datasets/rashadrmammadov/heart-disease-prediction)
