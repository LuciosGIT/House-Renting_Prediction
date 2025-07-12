# 🏠 Previsão de Preço de Aluguel de Casas em São Paulo

Este projeto tem como objetivo prever o preço de aluguel de casas no estado de São Paulo utilizando aprendizado de máquina supervisionado. Os modelos foram treinados com base no dataset `sao-paulo-properties-april-2019.csv`, que contém dados de propriedades listadas em abril de 2019.

## 📂 Dataset

- **Nome:** sao-paulo-properties-april-2019.csv  
- **Fonte:** Kaggle / Data Science Challenges  
- **Descrição:** O conjunto de dados inclui informações como número de quartos, banheiros, vagas, área útil, localização, tipo do imóvel, entre outros atributos relevantes para precificação.

## 📍 Visualização Geoespacial com Mapbox

O projeto também utiliza a **API do Mapbox** em conjunto com a biblioteca `plotly` para gerar **mapas interativos**, permitindo visualizar espacialmente a distribuição dos imóveis disponíveis para aluguel na cidade de São Paulo. Isso facilita a análise de regiões com maior concentração, valores médios por bairro e outras informações geográficas relevantes.

## 🎯 Objetivo

Desenvolver modelos de regressão capazes de prever o preço de aluguel com base nos atributos das propriedades.

## 🧠 Modelos Utilizados

Três algoritmos de regressão foram testados:

- `LinearRegression`
- `DecisionTreeRegressor`
- `RandomForestRegressor`

Todos os modelos foram avaliados utilizando **validação cruzada (cross-validation)** para garantir resultados mais robustos e evitar overfitting.

## ⚙️ Otimização de Hiperparâmetros

O `RandomForestRegressor`, que apresentou o melhor desempenho entre os modelos testados, foi posteriormente otimizado com o uso de **GridSearchCV**, buscando os melhores valores de parâmetros como:

- `n_estimators`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`

## 📝 Avaliação

As métricas de avaliação utilizadas foram:

- `R² Score`
- `RMSE (Root Mean Squared Error)`
- `MAE (Mean Absolute Error)`

O modelo final otimizado apresentou o melhor equilíbrio entre viés e variância, sendo escolhido como modelo principal para a previsão de preços.

## 🛠️ Tecnologias e Bibliotecas

- Python 3.10+
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn (para visualização)
- Jupyter Notebook (para experimentação)

## 📊 Resultados

O `Random Forest Regressor` com hiperparâmetros otimizados se destacou com:

- **R² score (validação cruzada)**
- **Redução significativa no RMSE e MAE** em comparação com os outros modelos testados.

## 🚀 Como Executar

 1. Clone o repositório:
   ```bash
   git clone https://github.com/LuciosGIT/House-Renting_Prediction
```
2. Crie e ative um ambiente virtual:
 ```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```
3. Instale as dependências:
```bash
pip install -r requirements.txt
```
4. Execute o notebook:
```bash
jupyter notebook House_Renting_Pipeline.ipynb
```

## 📌 Conclusão
Este projeto demonstra como técnicas de machine learning podem ser aplicadas de forma eficiente para resolver problemas reais de previsão de preços. O uso de validação cruzada e otimização com grid search foi essencial para garantir a qualidade do modelo final.

