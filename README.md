# desafio_indicium_imdb


# Previsão de Nota do IMDB - Análise e Machine Learning

Este projeto tem como objetivo explorar um dataset de filmes e criar um modelo preditivo para estimar a nota do IMDB a partir de características dos filmes.

---

## 📝 Conteúdo do Projeto

1. **Exploração de Dados (EDA)**
   - Visualização das principais variáveis do dataset.
   - Análise de correlação entre faturamento, votos, metascore e nota do IMDB.
   - Insights sobre sinopses (`Overview`) e palavras-chave mais frequentes por gênero.
   - Identificação de padrões para recomendação de filmes.

2. **Pré-processamento**
   - Tratamento de valores ausentes.
   - Conversão de colunas numéricas (`Runtime`, `Gross`, `Released_Year`) para tipo correto.
   - Normalização de variáveis numéricas com `StandardScaler`.
   - Codificação de variáveis categóricas (`Genre`, `Director`, `Stars`) com `OneHotEncoder`.
   - Remoção de stopwords e palavras genéricas de filmes para análise de Overview.

3. **Modelagem**
   - Problema tratado como **regressão** (previsão de nota contínua).
   - Modelos utilizados:
     - `LinearRegression`
     - `RandomForestRegressor`
     - `RidgeRegression`
     - `GradientBoostingRegressor`
   - Avaliação de desempenho com **RMSE** e **R²**.
   - Pipeline completo: pré-processamento + modelo para facilitar previsões de novos filmes.

4. **Previsão de Novos Filmes**
   - Exemplo: *The Shawshank Redemption*.
   - Aplicação do pipeline para prever a nota do IMDB.
   - Transformações automáticas de colunas numéricas e categóricas aplicadas pelo pipeline.

5. **Visualização e Insights**
   - Gráficos comparando métricas dos modelos (R² e RMSE).
   - Nuvens de palavras por gênero, mostrando termos mais frequentes em sinopses.
   - Identificação de fatores que influenciam o faturamento e a nota do IMDB.
   - Recomendação de filmes baseada em votos e nota média.

---

## ⚙️ Como Rodar o Projeto

1. Clonar o repositório:

```bash
git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_PROJETO>
