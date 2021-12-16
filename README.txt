#########################################################################

CBPF 2021.2
Big Data e Astroinformática
Profº Clécio de Bom

Aluno Maurício Marques Soares Filho 

#########################################################################

Projeto 07: "Where's Waldo?"

Este projeto foi concebido e efetivado no ambiente Google Colab e, portanto, foi testado nesse ambiente. Outras formas de utilizar a rotina vão demandar adaptação.

Como pode ser depreendido da Apresentação que segue junto a esse arquivo, utilizamos o S-PLUS para gerar dois catálogos:
- "catalogo01.fits", uma amostra de oito colunas (bandas u, g, r, i, z, F515, F660, F861) com as 100000 primeiras entradas do banco de dados dr1. Esse catálogo será usado no programa de busca de outliers;
- "catalogo02.fits", contendo todas as colunas para as 100000 primeiras entradas do banco de dados dr1.
Mantendo-se essa simetria entre os arquivos de entrada, a rotina trabalha de forma eficiente, mesmo se o primeiro arquivo contiver mais colunas (somente com entradas numéricas - entradas contendo caracteres alfabéticos travam, é claro, as rotinas).

ATENÇÃO: as rotinas podem apresentar saídas diferentes mesmo se não houver mudança no random_state - conforme uma das fontes do nosso trabalho, "your results may vary given the stochastic nature of the algorithm or evaluation procedure, or differences in numerical precision. Consider running the example a few times and compare the average outcome". Não se trata de um erro de implementação, portanto.

Se o pipeline for executado conforme a sequência, serão extraídos sete outliers, os mais excêntricos de cada grupo de dados nas condições dadas (a dinâmica pode ser bem entendida lendo-se os comentários das rotinas). No final, essas sete entradas do catalogo02.fits serão salvas no arquivo Results.csv, que pode ser lido e trabalhado no TOPCAT (lembre-se de designar a extensão .csv quando importar o arquivo), e os dados exportados para o ALADIN, por exemplo, para visualização e estudo.

A quantidade de outliers selecionados por rodada pareceu adequada aos fins propostos na atribuição do trabalho. Um número maior de dados vai demandar pequena mudança nas rotinas. Mas lembre-se, você sempre pode rodar o programa novamente e, se os dados e a aleatoriedade estiverem a seu favor, conseguir mais sete pontos diferentes!

#########################################################################  