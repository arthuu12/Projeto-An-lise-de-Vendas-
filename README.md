# Análise de Vendas da Amazon


Este projeto realiza uma análise exploratória de um conjunto de dados de vendas da Amazon. O objetivo principal é identificar quais produtos contribuem mais para o lucro em cada categoria, além de realizar uma limpeza nos dados para remover inconsistências e outliers.

## Problema

Analisar os produtos que mais contribuem para o lucro de cada categoria.

## Tecnologias Utilizadas

* **Python:** Linguagem principal para a análise de dados.
* **Pandas:** Para manipulação e análise dos dados em formato de DataFrame.
* **Matplotlib:** Para a criação de visualizações gráficas, como boxplots.
* **Google Colab:** Ambiente de notebook utilizado para desenvolver e executar o código.

## Estrutura do Projeto

O notebook está dividido nas seguintes seções:

1.  **Importação de Bibliotecas e Carregamento dos Dados:** Configuração inicial do ambiente e leitura do arquivo `Amazon-2_Raw.csv`.

2.  **Limpeza e Tratamento dos Dados:**
    * **Análise Inicial:** Verificação de informações básicas do DataFrame, como tipos de dados e valores nulos.
    * **Verificação de Duplicatas:** Checagem para garantir que não há registros duplicados.
    * **Análise de Variáveis Quantitativas:** Utilização do método `describe()` para obter uma visão estatística das colunas numéricas (Vendas, Quantidade, Lucro).
    * **Identificação e Remoção de Outliers:** Análise de boxplots para as colunas de "Vendas" e "Lucro" para identificar e remover dados discrepantes que poderiam distorcer a análise. Foram removidos:
        * Um produto na categoria "Copiers" com vendas de $13.999,96.
        * Um produto na categoria "Machines" com um prejuízo de -$3.399,98.

3.  **Análise por Categoria:**
    * Para cada categoria de produto, foi criada uma nova coluna **"% profit"** para calcular a porcentagem de contribuição de cada produto para o lucro total daquela categoria.
    * Os produtos foram então ordenados para identificar os que mais impactam o lucro.
