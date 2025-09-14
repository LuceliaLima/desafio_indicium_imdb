#  Desafio Técnico  LH_CD_Lucelia (Ciência de Dados)


# 🎬 Previsão de Nota do IMDB

Este projeto tem como objetivo explorar um dataset de filmes e criar um modelo preditivo para estimar a nota do IMDB a partir de características dos filmes.

---

## 🔹 Objetivos do Projeto

- **Recomendar filmes** com base na nota e número de votos.  
- **Identificar fatores que influenciam o faturamento**.  
- **Extrair insights da coluna Overview** e verificar relação com gênero.  
- **Prever a nota do IMDB** usando modelos de regressão.  
- **Visualizar resultados** com gráficos e nuvens de palavras.


## 📂 Estrutura do Projeto

📦 desafio_lighthouse_imdb

- │── `📂 data/` → Pasta com datasets
-   │       └── `desafio_indicium_imdb.csv` → dataset original
-   │       └── `imdb_tratado.csv` → dataset com versões tratadas, exportadas no EDA
- │── `EDA.ipynb` → Análise exploratória dos dados (limpeza, gráficos, insights)
- │── `modelagem.ipynb` → Preparação dos dados, treino, avaliação e exportação do modelo
- │── `pipeline.pkl` → pipeline treinado e salvo com o melhor modelo
- │── `README.md` → documentação do projeto

## ⚙️ Como Rodar o Projeto

1. Como clonar o repositório:
   
```
git clone https://github.com/LuceliaLima/desafio_lighthouse_imdb.git

```


Pré-requisitos
Python 3.13.5  ou superior

2. Instalar dependências:

```
pip install -r requirements.txt
```


## 📊 Análise Exploratória (EDA)

Abra o arquivo EDA.ipynb no Jupyter Notebook e execute as células.

Nessa etapa são realizadas:

- Carregando os dados original
- Limpeza e pré-processamento inicial
- Qualidade dos dados
- Análise univariada
- Análise bivariada
- Análise temporal
- Insights Texto (Overview)
- Atores, Diretores e Gênero
- Exportação dos dados tratados

```
jupyter notebook EDA.ipynb
```

## 🤖 Modelagem

Abra o arquivo Modelagem.ipynb e execute: 

- Carregando o dados tratados
- Seleção das variavéis
- Pré-processamento (imputação, StandardScaler, OneHotEncoder)
- Definição e Predição do Modelo
   - Modelos utilizados:
        - `LinearRegression`
        - `RidgeRegression`
        - `LassoRegression`
        - `RandomForestRegressor`
        - `GradientBoostingRegressor`
        - `XGBRegressor`
    - Métricas de avaliação: **RMSE** e **R²**
- Visualização dos modelos
- Salvando Melhor Modelo em pipeline.pkl


```
jupyter notebook modelagem.ipynb
```

Dentro deste notebook em modelagem.ipynb, há um exemplo de previsão com The Shawshank Redemption.



👩‍💻 Autora

Feito por Lucelia Lima  🚀



