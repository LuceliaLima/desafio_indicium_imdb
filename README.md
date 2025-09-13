#  Desafio Técnico  LH_CD_Lucelia (Ciência de Dados)


# 🎬 Previsão de Nota do IMDBg

Este projeto tem como objetivo explorar um dataset de filmes e criar um modelo preditivo para estimar a nota do IMDB a partir de características dos filmes.

---

## 📂 Estrutura do Projeto

IMDB_Prediction/
- │
- ├─ data/ # Dataset CSV
- ├─ notebooks/ # Notebooks de exploração e modelagem
- ├─ scripts/ # Scripts Python executáveis
- ├─ requirements.txt # Dependências
- └─ README.md # Este arquivo


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

### Exemplo de treino e previsão

```python
pipeline.fit(X_train, y_train)
preds = pipeline.predict(X_test)
rmse = np.sqrt(mean_squared_error(y_test, preds))
r2 = r2_score(y_test, preds)
print(f"RMSE: {rmse:.2f}, R²: {r2:.2f}")


📝 Exploração de Dados

Filmes recomendados:

- Insights do Overview: palavras mais frequentes, possibilidade de inferir gênero.

- Nuvens de palavras por gênero: visualização clara dos temas principais de cada gênero.

🚀 Previsão de Novos Filmes

shawshank = pd.DataFrame([{
    'Runtime': 142,
    'Meta_score': 80,
    'No_of_Votes': 2343110,
    'Gross': 28341469,
    'Certificate': 'A',
    'Genre': 'Drama',
    'Director': 'Frank Darabont',
    'Star1': 'Tim Robbins',
    'Star2': 'Morgan Freeman',
    'Star3': 'Bob Gunton',
    'Star4': 'William Sadler'
}])

pred_note = pipeline.predict(shawshank)[0]
print(f"Nota prevista do IMDB: {pred_note:.2f}")

📊 Visualizações

Comparação de R² e RMSE entre modelos.

Nuvens de palavras para cada gênero, destacando temas e enredos.

Gráficos de correlação entre faturamento, votos, metascore e nota do IMDB.

⚙️ Como Rodar o Projeto

Clonar repositório:

git clone <URL_DO_REPOSITORIO>
cd IMDB_Prediction








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
