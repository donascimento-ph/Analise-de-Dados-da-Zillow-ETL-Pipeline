# Projeto de Engenharia de Dados em Python com Zillow Rapid API, AWS e Apache Airflow

## Visão Geral

Este repositório contém um projeto de engenharia de dados que demonstra como construir e automatizar um processo ETL (Extração, Transformação e Carga) em Python. O projeto extrai dados de propriedades imobiliárias da Zillow Rapid API, carrega-os em um bucket Amazon S3 e, em seguida, aciona uma série de funções AWS Lambda para transformar os dados. Por fim, os dados transformados são convertidos em um formato de arquivo CSV e carregados em outro bucket do Amazon S3 usando o Apache Airflow. O Apache Airflow utiliza um operador S3KeySensor para monitorar se os dados transformados foram carregados em um bucket Amazon S3 antes de tentar carregar os dados em um cluster Amazon Redshift.

Uma vez que os dados são carregados no Amazon Redshift, o Amazon QuickSight é usado para visualizar os dados da Zillow Rapid API. O Apache Airflow, uma plataforma de código aberto para orquestrar e agendar fluxos de trabalho e pipelines de dados, desempenha um papel crucial neste projeto.

## Ferramentas Utilizadas

- Python
- Zillow Rapid API
- Amazon Web Services (AWS)

1. Amazon S3
2. AWS Lambda
3. Amazon Redshift
4. Amazon QuickSight

- Apache Airflow

## Dashboard no Amazon QuickSight

Para tornar os dados mais acessíveis e informativos, criamos um dashboard no Amazon QuickSight. Este painel oferece duas visualizações gráficas principais:

1. Gráfico de Média de Preço por Quantidade de Quartos:

Neste gráfico, representamos a relação entre a quantidade de quartos em um imóvel e o preço médio. Isso permite que os usuários vejam como os preços variam com base no número de quartos. A visualização ajuda na identificação de padrões, como se imóveis com mais quartos tendem a ser mais caros ou se existem exceções.

2. Gráfico de Mediana de Preço por Código Postal:

O segundo gráfico apresenta a mediana de preços agrupada por códigos postais. Isso fornece informações sobre como os preços imobiliários variam em diferentes áreas geográficas. A mediana é uma métrica robusta que ajuda a reduzir o impacto de valores atípicos, proporcionando uma visão mais precisa das tendências de preços em cada região.

<img src="Analise-de-Dados-da-Zillow-ETL-Pipeline
/DashboardQuickSight.jpg" alt="Dashboard QuickSight">



