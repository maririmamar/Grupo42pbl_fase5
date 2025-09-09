# FIAP – Faculdade de Informática e Administração Paulista

<p align="center">
  <a href="https://www.fiap.com.br/">
    <img src="docs/fiap.jpeg" alt="FIAP - Faculdade de Informática e Administração Paulista" width="40%">
  </a>
</p>

---

# Análise exploratória, identificação de tendências de produtividade e modelos preditivos para prever rendimento de safra

## 📌 Grupo: 42

## 👨‍🎓 Integrantes:
- Thiago Scutari – RM562831 | thiago.scutari@outlook.com  
- Henrique Ribeiro Siqueira – RM565044 | henrique.ribeiro1201@gmail.com  
- Mariana Cavalcante Oliveira – RM561678 | mari.kvalcant@gmail.com  

## 👩‍🏫 Professores:

### Tutor  
- Leonardo Ruiz Orabona  

### Coordenador  
- Andrei Godoi Chiovato  

---

## 📜 Descrição


Este projeto tem como objetivo principal construir e comparar modelos de machine learning para prever o rendimento de diferentes culturas agrícolas. A análise utiliza um conjunto de dados que contém informações sobre variáveis climáticas (precipitação, umidade, temperatura) e o tipo de cultura para prever o rendimento (`Yield`).

As etapas do projeto incluem:
* Análise Exploratória de Dados.
* Pré-processamento de Dados, incluindo a conversão da variável `Crop` através de One-Hot Encoding.
* Visualização de dados com Análise de Componentes Principais (PCA).
* Treinamento e avaliação de diferentes modelos de regressão: Regressão Linear, Random Forest Regressor, Regressão por Árvores de Decisão, XGBRegressor, SVR.



---

## 🧰 Tecnologias e Recursos

O projeto foi desenvolvido em Python e utiliza as seguintes bibliotecas:
* **pandas**: Para manipulação e análise de dados.
* **scikit-learn**: Para a construção de modelos de machine learning (Regressão Linear, Árvore de Decisão, Random Forest, SVR), pré-processamento de dados (StandardScaler) e PCA.
* **matplotlib** e **seaborn**: Para a criação de gráficos e visualizações.


---

## 📁 Arquivos do repositório

* **`Grupo42_pbl_fase5.ipynb`**: O notebook Jupyter que contém todo o código para a análise, pré-processamento, treinamento de modelos e visualização.
* **`crop_yield.csv`**: O conjunto de dados original utilizado para a análise e o treinamento dos modelos.

```

---

## ▶️ Como Executar
Para executar o projeto localmente, siga os seguintes passos:

1.  Certifique-se de ter o Python e as bibliotecas mencionadas instaladas. Se não as tiver, pode instalá-las via pip:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn
    ```
2.  Baixe o notebook `grupo42_pbl_fase5.ipynb` e o arquivo de dados `crop_yield.csv` no mesmo diretório.
3.  Abra o notebook em um ambiente Jupyter (Jupyter Notebook, JupyterLab, Google Colab, etc.).
4.  Execute as células do notebook sequencialmente para replicar toda a análise e o treinamento dos modelos.


---

### 📈 Resultados Principais

Foram identificados poucos outliers da variável Temperatura a 2 m (C) e houveram muitos outliers na variável Rendimento.

Os modelos de regressão testados demonstraram um alto poder preditivo, com o **Random Forest Regressor** apresentando o melhor desempenho geral, com o menor Erro Médio Absoluto (MAE).

* **Regressão Linear:** Excelente ajuste, com um R-squared de **1.00**.
* **Árvore de Decisão:** Bom ajuste, com um R-squared de **0.99**.
* **Random Forest:** Desempenho superior e robusto, com um R-squared de **0.99** e o menor MAE.
* **Análise PCA:** Durante a  visualização dos dados, foi identificado que as culturas no geral têm componentes principais similares (variações ambientais e rendimento da safra), já que houve sobreposição de agrupamentos. A cultura de Oil palm fruit não se sobrepõe como as demais, mas ainda assim, os pontos não estão tão distantes com relação às demais culturas.

Os modelos de treinamento com XGBRegressor e SVR também apresentaram bons coeficientes de Determinação (R-squared): 0.99.

A interpretação do resultado dos treinamentos também sugere que as variáveis Precipitação e Umidade específica possuem coeficientes positivos. Assim, um aumento da precipitação e da umidade específica podem indicar um maior rendimento.

As variáveis Temperatura e Umidade relativa possuem coeficientes negativos. Assim, um aumento da temperatura e da umidade relativa podem indicar um** menor** rendimento.

A cultura Oil palm fruit também demonstra um rendimento maior em relação a outras culturas que tiveram o coeficiente negativo. Isso se confirma com o gráfico de clusterização a partir do DBSCAN.


---

## 📽️ Demonstração e código

O vídeo de apoio se encontra na pasta`/video`.
Link youtube: https://youtu.be/Mb1mIyazTKY

Jupyter Notebook:
https://colab.research.google.com/gist/maririmamar/5cd8673c12cbf37eae5b9df839200551/grupo42_pbl_fase5.ipynb

---

## 📝 Licença

Creative Commons Attribution 4.0 International License  
[http://creativecommons.org/licenses/by/4.0](http://creativecommons.org/licenses/by/4.0)

---








