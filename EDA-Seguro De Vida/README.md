# dados_de_seguros

![capa_insurance.png](https://github.com/cecellhax/seguro-de-vida/blob/main/capa_insurance.png)

## Sobre os dados

### Colunas

**age:** idade do beneficiário principal

**sex:** sexo do contratante do seguro, feminino, masculino

**bmi:** Índice de massa corporal, fornecendo uma compreensão do corpo, pesos que são relativamente altos ou baixos em relação à altura, índice objetivo de peso corporal (kg / m ^ 2) usando a relação entre altura e peso, idealmente 18,5 a 24,9

**children:** Número de filhos cobertos pelo seguro saúde / Número de dependentes

**smoker:** indica se a pessoa é fumante ou não

**region:** área residencial do beneficiário nos EUA, nordeste, sudeste, sudoeste, noroeste

charges: despesas médicas individuais cobradas pelo seguro saúde

## Objetivos

O objetivo principal deste repositório é criar visualizações dos dados de custos médicos:

Esclarecer informações sobre o perfil da população;

Trazer reflexões baseadas em dados sobre os custos médicos e assim gerar insights para tomada de decisão em possíveis propostas de seguradoras.

## Documentos gerados

Sweetviz é uma biblioteca Python de código aberto que gera belas visualizações de alta densidade para iniciar o EDA (Exploratory Data Analysis) com apenas algumas linhas de código. A saída é um aplicativo HTML. O script principal está em [**analise_exploratoria.ipynb**](https://github.com/cecellhax/seguro-de-vida/blob/main/analise_exploratoria.ipynb) com o uso da biblioteca Switviz geramos os seguintes relatórios:
- [**relatorio_geral_dos_dados.html**](https://github.com/cecellhax/seguro-de-vida/blob/main/relatorio_geral_dos_dados.html)
- [**relatorio_filhos.html**](https://github.com/cecellhax/seguro-de-vida/blob/main/relatorio_filhos.html)
- [**relatorio_fumantes.html**](https://github.com/cecellhax/seguro-de-vida/blob/main/relatorio_fumantes.html)
- [**relatorio_sexo.html**](https://github.com/cecellhax/seguro-de-vida/blob/main/relatorio_sexo.html)

## Fontes dos dados

De [**Pycaret**](https://github.com/pycaret) dentres os datasets o arquivo [**insurance. csv**](https://github.com/pycaret/pycaret/blob/master/datasets/insurance.csv)

## Ferramentas utilizadas

[**Google Colaboratory;**](https://colab.research.google.com)

[**Pycaret;**](https://github.com/pycaret)

[**Sweetviz.**](https://pypi.org/project/sweetviz)

## Dependências

`pip install pycaret`

`pip install sweetviz`

#

*Pode ser observado o uso de algumas técnicas e funcionalidades de bibliotecas de manipulação e visualização de dados.*

*Conta com análises exploratórias, manipulação de dataframes e séries, plotagem de gráficos, entre outros.*

*Projeto desenvolvido durante o Workshop Dominando Data Science, da Flai Inteligência Artificial, ministrado pela Dra. em Estatística Juliana Scudilio.*
