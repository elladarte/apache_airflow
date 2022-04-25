# Rocket Images

## Sobre o Projeto:

O objetivo desse estudo é coletar as images dos foguetes dos proximos lançamentos, criando uma pipeline de extração e carregamento de dado usando o framework Apacha Airflow. Desta forma, é utilizado a Launch Library 2, uma API gratuita e aberta que contem dados sobre lançamentos de foguetes históricos e futuros de várias fontes (https://thespacedevs.com/llapi).

A Lauch Library 2 foi desenvolvida pelo The Space Devs, que é um grupo de desenvolvedores entusiastas do espaço que trabalham em uma variedade de serviços, unidos em um objetivo comum de melhorar o conhecimento público e a acessibilidade das informações de voos espaciais (https://thespacedevs.com/).

## Pré-requisitos:

## Instalação:
Criaçao do ambiente virtual com o pyenv para o desenvolvimento
```
python -m venv venv
source venv/bin/activate
```
Instalando o Airflow e suas dependencias 
```
pip install apache-airflow
```

## Execução:
Inicializando o metastore e criando um usuario
```
airflow db init
airflow users create --username username --password password --firstname firstname --lastname lastname --role Admin --email admin@example.org
```
Copiando o DAG de lançamento do foguete nos DAGs diretório
```
cp download_rocket_launches.py ~/airflow/dags/
```
Iniciando o agendador e o servidor web
```
airflow webserver
airflow scheduler
```

## Referencia:

GETTING started: Anatomy of an Airflow DAG. In: HARENSLAK, Bas; RUITER, Julian de. Data pipelines with Apache Airflow. 1. ed. [S. l.]: Manning Publications, 2021. cap. 2, p. 46-65. ISBN 9781617296901. Disponível em: https://b-ok.lat/book/11987823/93c9f5. Acesso em: 24 abr. 2022.

https://github.com/BasPH/data-pipelines-with-apache-airflow