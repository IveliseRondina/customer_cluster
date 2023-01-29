![kmeans](https://user-images.githubusercontent.com/103456938/215295758-5c829740-d256-42ae-9f9b-77c4bb1b9205.jpg)

<h1 align="center"> Cluster de clientes </h1>

Este projeto tem como objetivo principal agrupar clientes com base no seu comportamento, e fazer uma análise detalhada do perfil ideal de consumidores. O que facilita o melhor entendimento do negócio e seus consumidores, tornando mais fácil qualquer mudança de produto que possa ser necessária de acordo com necessidade específica, comportamento ou preocupações dos diferentes tipos de consumidores. 

O resultado foi atingido através da utilização do algorítmo Kmeans, um algorítmo de aprendizado não supervisionado que avalia e clusteriza os dados de acordo com suas características. 


## Características Iniciais

**People**

* ID: Identificação única do consumidor
* Year_Birth: Data de nascimento do consumidor
* Education: Nível educacional do consumidor
* Marital_Status: Estado Civil do consumidor
* Income: Salário anual do consumidor
* Kidhome: Número de crianças na casa
* Teenhome: Número de adolescentes na casa
* Dt_Customer: Data de inscrição do consumidor na empresa
* Recency: Número de dias desde a ultima compra
* Complain: 1 se o consumidor reclamou nos ultimos 2 anos, 0 caso contrário

**Products**

* MntWines: Quantia gasta em vinhos nos ultimos 2 anos
* MntFruits: Quantia gasta em frutas nos ultimos 2 anos
* MntMeatProducts: Quantia gasta em carne nos ultimos 2 anos
* MntFishProducts: Quantia gasta em peixe nos ultimos 2 anos
* MntSweetProducts: Quantia gasta em doces nos ultimos 2 anos
* MntGoldProds: Quantia gasta em ouro nos ultimos 2 anos

**Promotion**

* NumDealsPurchases: Número de compras feitas com desconto
* AcceptedCmp1: 1 se o cliente aceitou a oferta na 1ª campanha, 0 caso contrário
* AcceptedCmp2: 1 se o cliente aceitou a oferta na 2ª campanha, 0 caso contrário
* AcceptedCmp3: 1 se o cliente aceitou a oferta na 3ª campanha, 0 caso contrário
* AcceptedCmp4: 1 se o cliente aceitou a oferta na 4ª campanha, 0 caso contrário
* AcceptedCmp5: 1 se o cliente aceitou a oferta na 5ª campanha, 0 caso contrário
* Response: 1 se o cliente aceitou a oferta na última campanha, 0 caso contrário

**Place**

* NumWebPurchases: Number of purchases made through the company’s website
* NumCatalogPurchases: Number of purchases made using a catalogue
* NumStorePurchases: Number of purchases made directly in stores
* NumWebVisitsMonth: Number of visits to company’s website in the last month

## Premissas Assumidas

A análise inicial foi feita agrupando as características de pessoas, produtos, promoções e local. Após o tratamento inicial dos dados, o dataframe foi unificado.

Na análise de pessoas: 
* foram desconsiderados valores nulos de salario anual, uma vez que representavam um número infimo de amostras;
* desconsiderado um registro de salário anual superior a U$200.000;
* considerados ano de nascimento superior à 1930;
* estado civil Single, Alone e Yolo foram unificados;
* estado civil Together e Married foram unificados;

## Premissas de Negócio
Algumas variáveis tiveram pesos alocados diferentemente, com base nas premissas de negócio, como abaixo:
* TotalAmountSpent = 8
* TotalPurchases = 6
* Recency = 4
* NumWebVisitsMonth = 4
* Income = 4
* LifeTime = 4
* Year_Birth = 2
* ChildrenHome = 2
* Education = 2

As demais variáveis não tiveram pesos diferenciados.


## Conclusões























