# 🧠 User Reviews – Análise de Sentimentos com Naive Bayes

Este projeto tem como objetivo aplicar técnicas de **Análise Exploratória de Dados (EDA)** e **Aprendizado de Máquina (NLP + Naive Bayes)** para classificar o sentimento de avaliações textuais deixadas por usuários em cursos da plataforma [365 Data Science](https://365datascience.com/).

---
> Este projeto foi desenvolvido com fins de estudo sobre Processamento de Linguagem Natural (NLP) e o algoritmo Naive Bayes.  
> Pode conter erros, imprecisões ou simplificações. Sinta-se à vontade para sugerir melhorias!
---

## 📌 Objetivo

Identificar se os comentários deixados pelos usuários são **positivos ou negativos**, utilizando um modelo supervisionado de classificação de texto.

---

## 🔍 Etapas do Projeto

### 1. Importação e limpeza dos dados

- Leitura manual de arquivo `.csv` contendo 4 colunas: nome do usuário, data da review, nota de 1 a 5, e comentário textual.
- Conversão de tipos e tratamento de valores nulos, incluindo conversão da nota para numérico e tratamento de erros.
- Exclusão de registros incompletos, com erro de formatação ou valores ausentes.

### 2. Análise Exploratória (EDA)

- Remoção de linhas com valores ausentes e conversão de tipos de dados.
- Análise estatística das notas (média, desvio padrão, etc.).
- Distribuição das notas (ratings) em histograma.
- Criação de uma nova feature: comprimento do comentário.
- Cálculo de correlação entre a nota e o tamanho do texto.
- Identificação de padrões linguísticos nos comentários via regex (palavras positivas/negativas, uso de caixa alta, interrogações e exclamações).

### 3. Pré-processamento textual

- Limpeza dos comentários: remoção de pontuação e conversão para minúsculas.
- Detecção de padrões linguísticos por regex (ênfases positivas e negativas, uso de caixa alta, interrogações e exclamações).
- Vetorização dos comentários via **TfidfVectorizer**.

### 4. Criação do modelo de Machine Learning

- Conversão das notas em sentimentos binários:
  - Notas 4 e 5 → **Positivo**
  - Notas 1 e 2 → **Negativo**
  - Notas 3 foram excluídas por serem neutras.
- Divisão em treino e teste (80/20).
- Balanceamento das classes via oversampling.
- Treinamento de um classificador **Naive Bayes** para classificação multiclasse e binária.
- Avaliação com métricas: acurácia, matriz de confusão e classification report.
- Validação do modelo em conjunto de teste externo.

---

## 🛠️ Tecnologias Utilizadas

- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Regex)
- **NLP** com Scikit-learn: `TfidfVectorizer`, `MultinomialNB`
- Visualizações gráficas com `matplotlib`
- Análise de correlação entre variáveis quantitativas

---

## 📈 Resultados

O modelo Naive Bayes mostrou-se eficiente para classificar sentimentos com base em um vocabulário básico de palavras positivas e negativas, demonstrando como técnicas simples de NLP podem gerar bons insights a partir de dados textuais.

---

## 💼 Habilidades Demonstradas

- Limpeza e manipulação de dados com Pandas
- Visualização de dados para tomada de decisão
- Engenharia de atributos aplicada ao texto
- Classificação binária com modelo probabilístico
- Comunicação de resultados técnicos de forma clara e concisa

---

## 📂 Estrutura do Projeto

```
📁 projeto/
├── 365 User Reviews Naive Bayes Sentiment Analysis.ipynb
├── user_courses_review_09_2023.csv
└── README.md  ← (este arquivo)