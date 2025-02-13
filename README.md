# Classificação de Músicas do Spotify

Este projeto contém um notebook Python que classifica músicas do Spotify em duas categorias – **música agitada** e **música lenta** – com base em características extraídas de faixas musicais. A classificação é feita utilizando a coluna `valence` da base de dados, que indica o grau de positividade da música, e uma série de modelos de Machine Learning.

## Sumário

- [Sobre a Base de Dados](#sobre-a-base-de-dados)
- [Objetivo do Projeto](#objetivo-do-projeto)
- [Funcionalidades](#funcionalidades)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Pré-requisitos](#pré-requisitos)
- [Instalação e Execução](#instalação-e-execução)
- [Contribuição](#contribuição)
- [Licença](#licença)
- [Contato](#contato)

## Sobre a Base de Dados

A base utilizada é o **Spotify Tracks Dataset** disponível no Kaggle. Ela contém informações sobre faixas musicais em **125 gêneros diferentes**, com diversos recursos de áudio, como `danceability`, `energy`, `loudness`, `valence`, entre outros.

A base pode ser encontrada em:  
[Spotify Tracks Dataset - Kaggle](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)

## Objetivo do Projeto

O notebook tem como objetivo desenvolver um **modelo preditivo** que classifique as músicas em duas categorias com base na coluna `valence`:

- **Música Agitada:** Faixas com `valence` > 0.5 (mais positivas, enérgicas)
- **Música Lenta:** Faixas com `valence` ≤ 0.5 (mais calmas, introspectivas)

## Funcionalidades

- **Análise Exploratória dos Dados:** Visualização da distribuição da coluna `valence` e análise das correlações entre variáveis.
- **Criação da Variável Target:** Geração de uma coluna que categoriza as músicas como "agitada" ou "lenta" com base na valência.
- **Feature Engineering:** Tratamento de dados, remoção de colunas irrelevantes e label encoding para variáveis categóricas.
- **Divisão dos Dados:** Separação dos dados em conjuntos de treino e teste utilizando a técnica hold-out.
- **Normalização:** Aplicação do `MinMaxScaler` para escalonar os dados no intervalo [0, 1].
- **Modelagem:** Implementação e avaliação de diferentes modelos:
  - Regressão Logística
  - K-Nearest Neighbors (KNN)
  - Random Forest
- **Validação e Avaliação:** Utilização de métricas como AUC, Classification Report e a Curva ROC para avaliar a performance dos modelos.
- **Otimização de Hiperparâmetros:** Uso do Grid Search para encontrar os melhores parâmetros para o modelo Random Forest.
- **Previsão com Novos Dados:** Aplicação do modelo otimizado para classificar novas músicas a partir de um arquivo Excel (`novos_dados.xlsx`).

## Tecnologias Utilizadas

- **Linguagem:** Python
- **Bibliotecas:**
  - [pandas](https://pandas.pydata.org/)
  - [numpy](https://numpy.org/)
  - [matplotlib](https://matplotlib.org/)
  - [seaborn](https://seaborn.pydata.org/)
  - [scikit-learn](https://scikit-learn.org/stable/)

## Pré-requisitos

- Python 3.x instalado
- Ambiente para executar notebooks (Jupyter Notebook ou Google Colab)
- Arquivos necessários:
  - `dataset.csv` – Base de dados do Spotify
  - `novos_dados.xlsx` – Arquivo com novos dados para previsão

## Instalação e Execução

1. **Clone o Repositório:**

   ```bash
   git clone https://github.com/Erickllino/Spotify-Music-Predict.git
