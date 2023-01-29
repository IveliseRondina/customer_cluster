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

### Cluster 0:
Grupo de mais alto valor, com menor número de clientes. Além de terem uma alta renda e maior nível de educação, são os que mais compram, com ticket médio mais alto entre todos os grupos. Não costumam visitar tanto o website da empresa, nem comprar sempre através de promoções, pois preferem as compras por catálogo e diretamente na loja. As categorias preferidas são a de carnes e a de vinhos. A maioria não tem filhos em casa e são os clientes cadastrados há mais tempo.
 

### Cluster 1:
É um grupo jovem, com menor poder aquisitivo, que é o menos ativo entre todos eles. A empresa precisa tomar certo cuidado, pois estão churnando e deixando de comprar como antes. É o grupo que menos aceita as campanhas de promoção. É uma oportunidade importante para a empresa fazer campanhas de produtos mais destinados ao público infantil. Grupo que mais faz compras em promoções (%). Gostam de fazer compras pela loja física. São os que mais visitam o website. Gostam mais de gold prods do que os outros clusters de maior valor.


### Cluster 2:
É o cluster com clientes mais novos, com menor poder aquisitivo, porém são os mais ativos dentro da empresa. É o grupo que se cadastrou há menos tempo. Os clientes gostam de fazer compras em promoções. Gostam de fazer compras pela loja física. Gostam de visitar o website, provavelmente para buscar promoções. Gostam mais de gold prods do que os outros clusters de maior valor.


### Cluster 3:
É um grupo que realiza muitas compras, porém com ticket médio bem menor que o grupo anterior, mas ainda assim trazendo bastante receita para a empresa.  Os clientes têm um salário anual relativamente alto, são mais velhos e geralmente têm 1 filho em casa. É o grupo que mais aprecia a categoria de vinhos e que tem maior número de clientes.


![image](https://user-images.githubusercontent.com/103456938/215355072-1e55e66a-6573-422f-8f7a-905858384fd9.png)


![image](https://user-images.githubusercontent.com/103456938/215355105-7a63781a-e72e-4eaa-9c90-e74384c58856.png)


![image](https://user-images.githubusercontent.com/103456938/215355420-e7986c14-8455-4521-b45b-aa6442f47d74.png)


![image](https://user-images.githubusercontent.com/103456938/215356126-a8a7eae6-2440-449e-9e74-7965390c6ac3.png)


![image](https://user-images.githubusercontent.com/103456938/215356146-bf4f54e8-0aa3-4d99-abde-0cfcb26dfa47.png)


![image](https://user-images.githubusercontent.com/103456938/215356162-2f9d9695-46eb-469d-b4c2-16fe2c53a74d.png)















