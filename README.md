# Otimização de aplicações financeiras

#### Aluno: [Flavia Szczerbacki](https://https://github.com/BIFla/tcc_bimaster)
#### Orientador: [Felipe Borges](https://github.com/FelipeBorgesC)



Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".



### Resumo

No contexto de uma empresas de capital misto endividada, o objetivo desse trabalho é melhorar sua situação financeira, otimizando seu portfólio de investimentos, para otimizar os resultados nos vencimentos das dívidas. 
Para as opções de investimento foram considerados três papéis do Tesouro Direto (tesouro-prefixado, tesouro-IPCA e tesouros-SELIC) e um ativo privado. 


### Abstract


To help a leveraged company to improve its financial situation, optimizing its investments portfolio, to have the best results in the debt maturity. 
For the assets options, it was chosen three Government Bonds (fixed rate, inflation floating rate and basic interest rate) and one private asset. 
 
### 1. Introdução

A Petrobras tem, em seu plano de negócios, metas audaciosas de redução de seu endividamento. O objetivo deste trabalho foi escolher ativos financeiros com prazos de vencimento semelhantes aos prazos dos vencimentos das dívidas, e otimizar a alocação do fluxo de caixa disponível gerado a cada ano pela companhia, escolhendo as melhores opções de investmentos disponívies. 
As variáveis de mercado que influenciam as escolhas são: (1) a taxa de câmbio R$/USD$ (pois tanto a dívida, como grande parte da receita da empresa estão associados a preços internacionais), (2) o IPCA (a taxa de inflação oficial usada nos títulos do tesouro pré fixados) e (3) a SELIC (taxa de juros) utilizada nos títulos do tesouro pós fixados. Foram utilizadas algumas restrições para a otimização de como alocar o montante a ser aplicado nas melhores opções de investimento consideradas. 
O Banco Central do Brasil publica semanalmente o Relatório Focus, que resume as projeções de longo prazo do mercado para a economia, e é formulado a partir de pesquisas macroeconômicas realizadas por instituições finceiras, refletindo as expectativas de longo prazo o mercado. Este foi então, um insumo importante para o estudo.   

### 2. Modelagem

Foi utilizado o Relatório Focus (de 26/11/21)como insumo importante para modelar do comportamento das opções de investimento para os anos de 2022 a 2025.
Outro intrumento adicional utilizado foi a criação de cenários, complementando os dados do Relatório Focus, com a expectativa de longo prazo de dois bancos (Itaú e Santander de dez/21). 
Dessa forma, para as três variáveis utilizadas (taxa de câmbio R$/USD$, IPCA e Selic), foram criados três cenários, (1) pessimista (com percentil 10), (2) base (com a mediana)e (3)otimista (com percentil 90).
Foi feita então, a otimzação do porfólio de ativos escolhidos, para cada um dos cenários. Para a otimzação foi usado o solver do excel para achar a melhor distribuição entre os quatro tipos de ativos (tesouro-IPCA, tesouro-prefixado, tesouro-SELIC e o papel privado).
Foram introduzidas algumas restrições, para rodar a otimização: (1) o percentual da distribuição entre opções deveria ser um número inteiro; (2) diversificação entre as três opções do tesouro direto (tesouro-IPCA, tesouro-prefixdo e tesouro-SELIC) cada um com pelo menos 10% da carteira; (3) para o papel privado, a quarta opção de investimento, sua participação deveria se menor ou igual a 5%; e (4) a soma dos quatro tipos de aplicações deve totalizar 100%.


### 3. Resultados

As otimizações da alocação da carteira de investimentos no període de 4 anos(entre 2022 e 2025), para cada um dos cenários, se comportou da seguinte forma:
O tesouro-IPCA teve a mesma distribuição de alocação para os três cenários. Sendo 10% ano 1 e 75% da carteira nos anos 2 a 4. Esse resultado reflete a expectativa do mercado de alta inflacionária no médio e longo prazo.
O tesouro-SELIC, no cenário pessimista teve alocação mínima de 10% para o ano 4. Já nos cenários base e otimista, ficam com participação alta da SELIC na carteira. Em linha com a expectativa do mercado, da previsão de alta de curto prazo deste indicador.
O tesouro-prefixado, tem sua maior alocação de 75% no primero ano do cenário pessimista, e alocaçao baixa (entre 10 e 15%)nos demais anos e cenários base e otimista. Espelhando maior expectativa das altas do IPCA (no médio e longo prazos) e da SELIC (no curto prazo).
Para o título privado, os resultados foram de manter sua participação máxima na carteira de 5%, exceto no ano 3 dos cenários base e otimista, que ficaram com 0% de participação.

### 4. Conclusões

As otimizações obtidas para cada cenário foram coerentes com as melhores oportunidades de investimento em cada um dos cenários estimados. 
Com a rotina de trabalho estruturad
a possibilita revisões esporádicas. Com a devida atualização dos dados e das expectativas das projeções, gerando um produto final interessante para análise e tomada de decisão.Outros impactos que hoje ainda estão incertos, como a política de aumento de taxa de juros dos Banco Central dos Estados Unidos, podem alterar drasticamentes as expectativas. Necessitando acompanhamento e revisões das previsões e dos resultados.


Matrícula: 192.110.229

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
