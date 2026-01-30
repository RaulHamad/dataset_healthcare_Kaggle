## Español: Predicción de Resultados Médicos

# 🏥 Predicción de Resultados de Exámenes (Kaggle Healthcare Dataset)

Este repositorio contiene un proyecto completo de **Ciencia de Datos**, enfocado en el procesamiento, análisis y modelado de datos del sector salud. El objetivo principal es prever el resultado de exámenes de laboratorio (`Test Results`) con base en perfiles de pacientes y condiciones clínicas.

El proyecto fue estructurado en tres etapas principales, utilizando técnicas experimentales para lidiar con datos de baja correlación y alta complejidad.

---

### 1. Limpieza e Ingeniería de Datos (ETL)
**Archivo:** *[Archivo: 01_kaggle_project_cleaning.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/01_kaggle_project_cleaning.ipynb)*

* **Tratamiento:** Eliminación de 534 registros duplicados.
* **Codificación:** Uso de Label y One-Hot Encoding para datos categóricos.
* **Escalamiento:** Normalización con `StandardScaler`.

### 2. Benchmark de Modelos y Evaluación
**Archivo:** *[Archivo: 02_Kaggle_Classificadores.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/02_Kaggle_Classificadores.ipynb)*

* **Modelos:** Naive Bayes, KNN, Árboles de Decisión, Random Forest, Gradient Boosting y MLP.
* **Hallazgo:** Los modelos basados en árboles superaron a los lineales.

### 3. Experimentación Avanzada y Optimización
**Archivo:** *[Archivo: 03_Modeling_and_Experimentation of Classifiers.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/03_Modeling_and_Experimentation%20of%20Classifiers.ipynb)*

* **Subespacio Aleatorio:** Creación de 10 datasets para filtrar "ruido" de atributos.
* **Validación:** K-Fold (10 pliegues) para solidez estadística.
* **Optimización:** **43.81% de precisión** alcanzado mediante `GridSearchCV`.

![](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/images/grafico.png)

### 4. Escalamiento Sintético y Curva de Aprendizaje (SMOTE)
**Archivo:** *[04_Experimental_Focus.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/04_Experimental_Focus.ipynb)*

Nesta fase, investigamos o impacto do volume de dados na performance dos modelos utilizando o subespaço otimizado de 40% de atributos.

* **Metodologia:** Expansão do dataset de 38k para 100k instâncias utilizando **SMOTE** para gerar dados sintéticos e **Resampling** para reduções estratégicas.
* **Objetivo:** Identificar o "ponto de saturação" onde dados sintéticos deixam de ajudar e começam a introduzir ruído.
* **Ponto Ótimo:** A melhor performance foi atingida com **50.000 instâncias**, elevando a acurácia para **42.03%**.

#### 📈 Curva de Aprendizado
O gráfico abaixo ilustra a evolução da acurácia. Note que após as 50k instâncias, a performance começa a degradar, caracterizando o **Overfitting Sintético**.

![Gráfico de Curva de Aprendizado](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/images/04_grafico.png)


---

## English: Test Results Prediction

# 🏥 Test Results Prediction (Kaggle Healthcare Dataset)

This repository contains a complete **Data Science** project focused on the processing, analysis, and modeling of healthcare sector data. The primary goal is to predict laboratory test results (`Test Results`) based on patient profiles and clinical conditions.

The project was structured into three main stages, utilizing experimental techniques to handle low-correlation and highly complex data.

---

### 1. Cleaning and Data Engineering (ETL)
**File:** *[01_kaggle_project_cleaning.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/01_kaggle_project_cleaning.ipynb)*

* **Data Handling:** Removal of 534 duplicate records.
* **Encoding:** Applied Label and One-Hot Encoding for categorical data.
* **Scaling:** Used `StandardScaler` for numerical normalization.

### 2. Model Benchmark and Evaluation
**File:** *[02_Kaggle_Classificadores.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/02_Kaggle_Classificadores.ipynb)*

* **Tested Models:** Naive Bayes, KNN, Decision Tree, Random Forest, Gradient Boosting, and MLP.
* **Key Finding:** Tree-based models outperformed linear ones, capturing non-linear clinical relationships.

### 3. Advanced Experimentation and Optimization
**File:** *[03_Modeling_and_Experimentation of Classifiers.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/03_Modeling_and_Experimentation%20of%20Classifiers.ipynb)*

* **Random Subspace:** Tested 10 datasets (30-80% density) to reduce noise.
* **Cross-Validation:** 10-fold validation for statistical robustness.
* **Tuning:** Achieved **43.81% accuracy** using `GridSearchCV` with Random Forest.

![](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/images/grafico.png)

### 4. Synthetic Scaling and Learning Curve (SMOTE)
* **File:** *[04_Experimental_Focus.ipynb]*
* **Methodology:** Expanded training set using **SMOTE** to find the saturation point.
* **Result:** Optimal accuracy reached at **50,000 instances (42.03%)**.

  
---

# 🏥 Predição de Resultados de Exames (Kaggle Healthcare Dataset)

Este repositório contém um projeto completo de **Ciência de Dados**, focado no processamento, análise e modelagem de dados do setor de saúde. O objetivo principal é prever o resultado de exames laboratoriais (`Test Results`) com base em perfis de pacientes e condições clínicas.

O projeto foi estruturado em três etapas principais, utilizando técnicas experimentais para lidar com dados de baixa correlação e alta complexidade.

---

## 🚀 Fluxo de Trabalho (Data Science Pipeline)

### 1. Limpeza e Engenharia de Dados (ETL)
**Arquivo:** *[01_kaggle_project_cleaning.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/01_kaggle_project_cleaning.ipynb)*

Nesta etapa inicial, o foco foi transformar dados brutos em um formato otimizado para algoritmos de Machine Learning:
* **Tratamento de Dados:** Identificação e remoção de 534 registros duplicados.
* **Codificação de Variáveis:** Aplicação de **Label Encoding** e **One-Hot Encoding** para converter dados categóricos (Gênero, Tipo Sanguíneo, Condição Médica) em formato numérico.
* **Escalonamento:** Uso de `StandardScaler` para normalizar atributos numéricos, garantindo que variáveis como "Idade" e "Valor da Conta" estejam na mesma escala.
* **Persistência:** Utilização da biblioteca **Pickle** para salvar os objetos processados, garantindo a reprodutibilidade entre notebooks.

### 2. Benchmark de Modelos e Avaliação
**Arquivo:** *[02_Kaggle_Classificadores.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/02_Kaggle_Classificadores.ipynb)*

Avaliação sistemática de múltiplos algoritmos para estabelecer uma linha de base (baseline):
* **Modelos Testados:** Naive Bayes, KNN, Decision Tree, Random Forest, Gradient Boosting e MLP (Redes Neurais).
* **Metodologia:** Divisão treino/teste e análise via **Matriz de Confusão** e F1-Score.
* **Descoberta:** Identificamos que modelos baseados em **árvores (Random Forest/Decision Tree)** superaram modelos lineares, indicando uma relação não-linear entre os sintomas e os resultados.

### 3. Experimentação Avançada e Otimização
**Arquivo:** *[03_Modeling_and_Experimentation of Classifiers.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/03_Modeling_and_Experimentation%20of%20Classifiers.ipynb)*

Focada em extrair o máximo de performance através de técnicas de pesquisa científica:
* **Random Subspace (Subespaço Aleatório):** Criação de 10 datasets variando a densidade de atributos (de 30% a 80%) para identificar quais colunas geravam "ruído" no modelo.
* **Validação Cruzada (K-Fold):** Uso de 10-folds para garantir que a acurácia fosse estatisticamente sólida e não fruto do acaso.
* **Hyperparameter Tuning:** Implementação de `GridSearchCV` para otimizar o Random Forest, alcançando a melhor performance documentada de **43.81% de acurácia** (em um cenário desafiador de 3 classes).

![](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/images/grafico.png)

  ### 4. Escalonamento Sintético e Curva de Aprendizado (SMOTE)
**Arquivo:** *[04_Experimental_Focus.ipynb](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/04_Experimental_Focus.ipynb)*
* **Metodologia:** Expansão do dataset de 38k para 100k instâncias via **SMOTE**.
* **Ponto Ótimo:** A melhor performance foi atingida com **50.000 instâncias** (acurácia de **42.03%**).
* **Insight:** O aumento excessivo (100k) gerou "Overfitting Sintético", degradando a performance.

![Curva de Aprendizado](https://github.com/RaulHamad/dataset_healthcare_Kaggle/blob/main/images/04_grafico.png)

---

