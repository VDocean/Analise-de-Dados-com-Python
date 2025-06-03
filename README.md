
# Introdução a Séries Temporais
 

Como o próprio nome sugere, séries temporais são o registro de algum dado ao longo do tempo que quando analisados geram informação a cerca de determinado assunto. Como exemplo podemos citar o registro de temperatura da superfície do mar, usados para prever eventos climáticos como ciclones, tempestades, frentes frias, el niño, entre outros. Exemplo:



[![](https://ciclovivo.com.br/wp-content/uploads/2023/04/temperatura-superficie-oceanos-2.jpg)](https://ciclovivo.com.br/planeta/crise-climatica/superficie-dos-oceanos-atinge-temperatura-recorde/)
  
  
# Componentes de uma Série Temporal

**Tendência** 

Refere-se ao comportamento dos dados a longo prazo que pode ser ascendente, descendente ou estável. Os tipos mais comuns são de tendência linear, constante e quadrática.  


![](/img/tendencia%20em%20series%20temporais.png)  

**Sazonalidade**  

É a repetição de padrões ao longo de intervalos de tempo definidos como dias, meses ou anos. Ex: volume de chuva ao longo do ano.

**Ciclo**  

São alterações que ocorrem na série de dados em intervalos não definidos. Por exemplo: crise econômica.

**Erro**  

Não possui uma relação matemática na série, sem padrão específico. Ex: interferência do atrito do substrato marinho na amplitude de maré.

# Correlação

É o estudo da relação entre duas váriáveis. A força dessa relação pode ser medida via coeficiente de Pearson com valores que variam de 1 a -1.  
* 1: relação linear perfeita, ambas as variáveis ascendem ou decrescem simultaneamente.  
* -1: perfeita correlação negativa, ou seja, enquanto uma variável aumenta a outra diminui.  
* 0: variáveis independentes, sem correlação. Também é chamado de ruído branco.


# Autocorrelação

É a análise da relação de uma série temporal com seus próprios valores em intervalos de tempos diferentes(lag).  
* Lag 1 correlaciona os valores do intervalo escolhido com os valores correspondente do intervalo anterior a ele.
* Lag 2 correlaciona os valores do intervalo escolhido com os valores correspondente a dois intervalos anteriores a ele.

# Regressão linear

A regressão linear é uma técnica estatística que modela a relação entre uma variável dependente e uma ou mais variáveis independentes.
Por exemplo temos a densidade da água do mar que depende dos valores de temperatura e salinidade. Portanto se tiver um conjunto de dados 
com esses valores posso modelar a relação entre eles de forma a descrever o comportamento dessas propriedades da água do mar.
Ao modelar essa relação é criado um conjunto de valores chamada de linha de ajuste e os valores da amostra usados para criá-la e que estão fora dos valores da linha de melhor ajuste são chamados de  
residuais. Ao usar esse conjunto de dados para tentar prever os valores de densidade a partir de um conjunto já existente corro risco de existirem erros nesta estimativa que podem ser mensurados através da comparação entre o valor previsto e dados reais.

**Algumas métricas de erros:**

* Erro Médio Absoluto (MAE): média absoluta das diferenças entre os valores previstos e os valores reais observados. Dá o erro na unidade de interesse.
* Erro Médio Quadrático (RMSE): é a raiz quadrada da média dos quadrados das diferenças entre os valores previstos e os valores observados.
* Erro Médio Absoluto Escalado (MASE): é uma métrica que compara o erro absoluto médio do modelo com o erro absoluto médio de um modelo de referência.
* Erro Médio Percentual Absoluto (MAPE): mede a precisão em termos percentuais, calculando a média dos erros percentuais absolutos.

# Decomposição 

Trata-se de separar cada um dos componentes de uma série temporal para compreendê-la melhor isolando valores de tedência, ciclo, sazonalidade e ruído.
Um exemplo é decomposição da série histórica da concentração de dióxido de carbono na atmosfera indicado abaixo:  

![](/img/decomposicao.png) 


# Tipo de Dados e Visualização

## Diferentes tipos de dados 

**Qualitativo**  : se refere aos atributos não numéricos como cor, 
**Quantitativo**: dados numérico. Exemplo: número de pessoas em uma plateia, temperatura corporal..
**Ordinal**  : qualitativo e quantitativo ao mesmo tempo. Uso um valor numérico para expressar qualidade, por exemplo posnutação dos clientes referente a um produto.

# Tipos de gráficos para dados quantitativos


 **Gráfico de pizza** 

  Usado para demonstrar percentagem de elementos que participam de um todo. Indicado quando a visualização dos dados exige menos precisão.

![](/img/graficos%20de%20pízza.jpg) 

**Gráfico de barras**  

  Adequado para demonstrar categorias.

![](/img/barras.png)

**Gráfico de linhas**

 Útil para séries temporais

![](/img/Grafico-de-linhas-no-Excel.png)
 

A análise pode ser somente de uma variável quantitativa ou da relação dela com relação a outras variáveis. 
Para isto podem ser usados os gráficos a seguir:

**Histograma**

Gráfico de frequência

![](/img/histograma.jpg)

**Boxplot**

![](/img/boxplot.png)

Explicação sobre o gráfico boxplot 

![](/img/explicação%20box%20plot.png)

# Características e Condições de Séries Temporais

## Erros

Diferença na comparação entre o valor previsto e medido.

Formas de medir o erro:

* Separando dados para testes
* Avaliando após a ocorrência do evento
* Com os próprios dados

Técnicas para avaliar erros:

## **Hold - out**

Em uma serie de dados 70% dos dados são usados para construção do modelo e os 30% restante para teste do modelo construído.

![](/img/houldout.jpg)

## **Cross Validation**

Consiste em dividir o conjunto de dados em um número de iteraçãoes e em cada iteração um conjunto de dados são usados para teste e o restante para treinamento.

![](/img/CrossValidation.png)

# Métricas de Erros em Previsões

medem a diferença entre o erro e o acerto

# **Erro médio (MSE)**

*os dados precisam ser na mesma escala*

é a média da diferença entre os valores medidos e simulados.
Limitação: sujeito as variações positivas e negativas dos valores que podem se anular.

![](/img/mse.png)

# **Erro médio absoluto (MAE)**

*dependemente de escala*

média das diferenças absolutas entre o medido e o previsto.

![](/img/mae.png)

# **Erro quadrático médio (RMSE)**

*Independe de escala*

Desvio padrão do previsto e do medido

![](/img/rmse2.png)

# **Erro médio percentual**

*independente de escala*

diferença percentual de erro

![](/img/mpe.png)

# **Erro médio percentual absoluto**

*Independe de escala*

diferença percentual absoluta de erro

![](/img/mape.png)

## Séries Temporais Estacionárias

Média e variância se matêm constante com o tempo.

# Médias Móveis

Processo de transformação de uma série através da retirada e de sazonalidade, tendências e outliers que resultam em uma suavização da série original. Dois tipos de métodos de aplicação de média móvel: simples e exponecial.

A ordem de uma média móvel define qual o intervalo antes e depois do valor de 
interesse serão usados para gerar a nova série.Quanto maior a ordem, maior a suavização.

![](/img/mediamovel.png)


# Referências:  📚
Fernando Amaral, Minerva Singh. Séries Temporais e Analises Preditivas com Python. Udemy: https://capgemini.udemy.com/course/series-temporais-com-python  
https://www.maxwell.vrac.puc-rio.br/4244/4244_5.PDF  


## Etiquetas

Adicione etiquetas de algum lugar, como: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)