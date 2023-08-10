# Titanic
Análise do conjunto de dados do Titanic disponível no [Kaggle](https://www.kaggle.com/competitions/titanic)

A trajetória dos resultados é apresentada a seguir e está acessível no [Kaggle](https://www.kaggle.com/raquelcunha)
<img src='https://github.com/Raqueljkl1/Titanic/blob/main/img/Line%20Graph%20-%20Blank%20Presentation%20(6).png'>


## **[Etapa 1: Inicial Model Development](https://github.com/Raqueljkl1/Titanic/blob/main/An%C3%A1lise_do_Titanic_Parte_1.ipynb)**

Nesta primeira fase, foram realizados procedimentos básicos para avaliar os resultados sem efetuar tratamentos ou engenharia de dados extensivos. Um resumo da base foi obtido utilizando a biblioteca ydata-profiling, que gera descrições detalhadas do conjunto de dados em poucas linhas. Colunas com alta cardinalidade foram eliminadas e valores vazios foram tratados através da substituição pela média e moda das variáveis. Colunas de texto foram removidas. Modelos foram criados empregando três algoritmos: Árvore de Classificação, KNN e Regressão Logística. A avaliação dos modelos abrangeu acurácia e matriz de confusão. O resultado público do Kaggle foi 0,66746.

## **[Etapa 2: Text Variable Processing](https://github.com/Raqueljkl1/Titanic/blob/main/Analise_do_Titanic_Parte_2.ipynb)**

Nesta fase subsequente, o foco foi o tratamento das variáveis de texto, permitindo a inclusão de todas elas no modelo. Através do uso de lambda functions e OneHotEncoder, os modelos prévios foram reaplicados. O score público do Kaggle melhorou para 0,76555.

## **[Etapa 3: Enhanced Data Treatment and Business Understanding](https://github.com/Raqueljkl1/Titanic/blob/main/An%C3%A1lise_do_Titanic_Parte_3.ipynb)**

A terceira etapa visava uma compreensão mais profunda dos dados para aprimorar seu tratamento e buscar melhorias nos resultados. Foram realizadas a normalização das colunas Age e Fare, assim como a criação de novas colunas relacionadas às colunas SibSp (nº de irmãos/cônjuges a bordo do Titanic) e Parch (nº de pais/filhos a bordo do Titanic). Uma análise de correlação levou à seleção das variáveis mais relevantes para o modelo. Os algoritmos previamente utilizados foram mantidos. O score público do Kaggle melhorou para 0,77033.

## **[Etapa 4: Exploring Alternative Algorithms](https://github.com/Raqueljkl1/Titanic/blob/main/An%C3%A1lise_do_Titanic_Parte_4.ipynb)**

Nessa fase, todas as colunas foram mantidas, incluindo SibSp e Parch. Novos algoritmos foram introduzidos para avaliar o desempenho do modelo. Além da Regressão Logística (que mostrou melhores resultados anteriormente), o RandomForest e o MLPClassifier (Redes Neurais) foram utilizados. Embora o MLPClassifier tenha demonstrado alta acurácia nos dados de validação, o resultado nos dados de teste indicou overfitting. O score público do Kaggle foi 0,69856.

## **[Etapa 5: GridSearchCV and Parameter Tuning](https://github.com/Raqueljkl1/Titanic/blob/main/An%C3%A1lise_do_Titanic_Parte_5.ipynb)**

Nesta etapa, o GridSearchCV foi empregado para otimizar os parâmetros dos modelos usados anteriormente. O modelo escolhido foi o RandomForest, e os resultados melhoraram significativamente em relação à etapa 4, superando também o desempenho da etapa 3. O score público do Kaggle foi 0,78229.
