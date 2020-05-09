# Identificar Perfil de Consumo de Clientes de uma Instituição Financeira

Uma Instituição Financeira X tem o interesse em identificar o perfil de gastos dos seus clientes. Identificando os clientes certos, eles podem melhorar a comunicação dos ativos promocionais, utilizar com mais eficiência os canais de comunicação e aumentar o engajamento dos clientes com o uso do seu produto. 

Os dados estão anonimizados por questões de segurança. No dataset, temos o valor gasto de 121818 clientes, no ano de 2019, em cada ramo de atividade. A base já está limpa. O intuito aqui é apresentar uma possibilidade de fazer a clusterização de clientes com base emm seu consumo, em código Python. Os dados são de 1 ano a fim de diminuir o efeito da sazonalidade.


### Modelagem não supervisionada

Ao utilizarmos um algoritmo de aprendizagem de máquina não supervisionado, não possuímos dados de entrada e de saída. Estamos interessados em encontrar padrões e relações em um cojunto de dados. Por isso, é uma abordagem utilizada, por exemplo, para traçar perfil de consumo dos clientes através do histórico de compras. 

Utilizaremos o percentual de gasto dos clientes em cada ramo. Com isso, obtivemos muitos valores zero. Para retirar o efeito desses valores, trasnformamos as variáveis numéricas em categóricas. 

Para dados categóricos, teremos que aplicar um método de clusterização chamado K-modes que foi publicado em 1998 por Zhexue Huang e portanto, tem pouca documentação. Sabemos que esse método é uma extensão do método K-means. Em vez de distância, ele usa dissimilaridades (isto é, quantificação das incompatibilidades totais entre dois objetos: quanto menor esse número, mais semelhantes são os dois objetos). E, em vez de médias, ele usa moda. Teremos tantas modas quanto o número de clusters necessários, pois eles atuam como centróides.

