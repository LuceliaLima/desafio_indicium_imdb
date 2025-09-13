#  Desafio Técnico  LH_CD_Lucelia (Ciência de Dados)


# 🎬 Previsão de Nota do IMDBg

Este projeto tem como objetivo explorar um dataset de filmes e criar um modelo preditivo para estimar a nota do IMDB a partir de características dos filmes.

---

## 📂 Estrutura do Projeto

📦 desafio_lighthouse_imdb
- │── data/ # Dados utilizados
- │ └── desafio_indicium_imdb.csv
- │── EDA.ipynb # Análise exploratória de dados
- │── modelagem.ipynb # Construção e avaliação do modelo
- │── pipeline.pkl # Modelo salvo
- │── requirements.txt # Dependências do projeto
- │── README.md # Este arquivo


---

## 🔹 Objetivos do Projeto

- 🎯 **Recomendar filmes** com base na nota e número de votos.  
- 💰 **Identificar fatores que influenciam o faturamento**.  
- 📝 **Extrair insights da coluna Overview** e verificar relação com gênero.  
- 🤖 **Prever a nota do IMDB** usando modelos de regressão.  
- 📊 **Visualizar resultados** com gráficos e nuvens de palavras.

---

## 🧹 Pré-processamento

- Limpeza de colunas numéricas (`Runtime`, `Gross`, `Released_Year`).  
- Remoção de stopwords e palavras genéricas de filmes (`movie`, `film`, etc.).  
- Normalização de numéricas (`StandardScaler`) e codificação de categóricas (`OneHotEncoder`).  
- Pipeline unificado para pré-processamento + modelo.

---

## 🤖 Modelagem

- Problema tratado como **regressão** (nota contínua).  
- Modelos utilizados:
  - `RandomForestRegressor`
  - `LinearRegression`
  - `RidgeRegression`
  - `GradientBoostingRegressor`
- Métricas de avaliação: **RMSE** e **R²**.  



## ⚙️ Como Rodar o Projeto





Pré-requisitos
Python 3.10 ou superior
Pip (gerenciador de pacotes do Python)

Instale as dependências:

pip install -r requirements.txt

Execute a Análise e a Modelagem: Para visualizar a Análise Exploratória dos Dados e todo o processo de criação do modelo, abra e execute o Jupyter Notebook modelagem.ipynb.
```bash
jupyter notebook EDA.ipynb
Dentro deste notebook, você encontrará a resposta para a previsão da nota do IMDB do filme "The Shawshank Redemption".

jupyter notebook modelagem.ipynb
Dentro deste notebook, você encontrará a resposta para a previsão da nota do IMDB do filme "The Shawshank Redemption".

(Opcional) Execute o Preditor via Script: O arquivo pipeline.py foi configurado para carregar o modelo (pipeline.pkl) e realizar previsões. Para executá-lo, utilize o terminal:

python pipeline.py




Clone este repositório:

git clone https://github.com/SEU-USUARIO/desafio_indicium_imdb.git
cd desafio_lighthouse_imdb

