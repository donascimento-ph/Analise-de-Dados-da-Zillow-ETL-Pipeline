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
