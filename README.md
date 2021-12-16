# AstroStatistic2021class
This repository concentrates the codes and notebooks related to the final term projects of AstroStatistics and Big Data lectures at CBPF for 2021.b (professor Clecio R. Bom). You can find the description of each project below. For further info on www.clearnightsrthebest.com 

## Projeto 01 - Strong Lensing Simulations with Lenstronomy
Grasiele

### Introduction

Strong lenses is a phenomenon that occurs when the light of a distant galaxy suffers a distortion when passing by a massive object (such as another galaxy or a galaxy cluster). These systems are exceptionally interesting because of the magnification effect, which allows us to observe objects that are even farther in the universe. Nevertheless, the study of such objects can be extremely expensive, due to the amount of time required in the large telescopes for the observation of it. Alternatively, the study of a synthetic population is extensively cheaper and it can  assist us in the understanding of observed systems. 

In this work I intend to create a simulated sample of strong lenses using the deeplenstronomy library in python. Additionally, in order to assure that these computationally created systems can exist in the real universe, I shall compare it to an observed sample of strong lensing. 


### GOAL


Produce a set of Strong Lensing simulations, either SL quasar population or for any lens in a given survey. You may use some lensing parameter distributions from Lenspop.


SL = Strong Lensing


## Project 02 - Probability Density Function compression
Pedro Riba

### Objetivo:

O armazenamento e a transmissão de dados pode ser um dos gargalos no estudo de astronomia e cosmologia, conforme o volume de dados aumenta. O objetivo do atual projeto é entender e aplicar duas técnicas diferentes para compressão da distribuição de densidade de probabilidade (PDF) de redshift fotométrico, a técnica de “Principal Component Analysis” (PCA) e o auto-enconder.

### O que farei:

Começarei estudando um exemplo simples, uma distribuição gaussiana de redshift fotométrico. Aplicarei a técnica de PCA e o auto-enconder para comprimir as PDF’s. Após, em um conjunto de dados mais realistas para redshift fotométrico, aplicarei as mesmas técnicas. Para avaliar a qualidade da compressão realizada utilizarei dois métodos distintos. Primeiramente analisarei o “Bayesian Information Criterion" (BIC) da distribuição após a compressão e antes da compressão. Além disso, analisarei a qualidade de compressão calculando a entropia relativa - ou divergência de Kullback-Leibler - entre as duas distribuições. Essa divergência serve de forma análoga a uma “distância” entre duas distribuições, sendo assim, nos dá informações importantes sobre o quão boa em manter o caráter principal dos dados é a técnica de compressão utilizada. 


## Project 03 - MAP a survey Depth
(André Santos)

### Introduction

An astronomical survey is a general map or image of a region of the sky that lacks a specific observational target. It may comprise a set of images, spectra, or other observations of objects that share a common type or feature. It is often stored in the form of fits tables, containing all the data converted from photometrics observations. Sky surveys are important because they allow astronomers to catalog celestial objects, perform statistical analyses on them and also search for transient astronomical events or other astrophysical subjects of interest.

### goal

The goal is to produce an estimated depth map for a survey calculating the limit magnitude. In particular, I’m going to use the dr9 dataset for the DESI Legacy survey.

### What i’m going to do?

First we start by clearing the dataset, treating non-physical measures, such as negative flux, or any NaN/Null values that may be present. Next we  get the magnitude in the current bands and calculate the associated invariance. After that, we calculate the limit magnitude and the associated error for the specific survey.

### References:
https://www.legacysurvey.org/dr9/description/
https://ui.adsabs.harvard.edu/abs/2019AJ....157..168D/abstract
https://www.legacysurvey.org/dr9/catalogs/#region-tractor-aaa-tractor-brick-fits
Ivezić, Željko, et al. Statistics, data mining, and machine learning in astronomy: A practical python guide for the analysis of survey data. Princeton University Press, 2019.


## Project 03 - Bayesian inference of H0 from simulated time delays
 (Arthur)


### Introdução
Time de delay é uma forma de medir a diferença de tempo de um sistema de lente gravitacional. Se objetos como quasares ou supernovas são afetados por lentes gravitacionais fortes, sua frente de onda de propagação se divide ao passar por esse objeto massivo (lente), formando múltiplas imagens. Além disso, essas imagens aparecem em tempos diferentes devido às diferentes geometrias entre os caminhos que a luz percorre, chegando em tempos diferentes ao observador. Ou seja, time delay é a diferença de tempo de chegada entre as imagens formadas. Nesse sentido, podemos medir essa diferença de time delay para fazer uma estimativa da constante de Hubble que é sensível a diferença de tempo dessas imagens múltiplas.

### Objetivo
Obter uma estimativa da constante de Hubble através da análise de um conjunto de parâmetros necessários para fazer simulações de time delay, para depois fazer uma inferência bayesiana desses dados e estimar a constante de Hubble.
### O que eu vou fazer?
Primeiro vamos utilizar as informações de um conjunto de dados contendo determinados parâmetros, tais como o ângulo de Einstein e red-shifts da lente e da fonte, necessários para encontrar um sistema de lentes gravitacionais que formam múltiplas imagens, e com isso podemos determinar o time delay desses sistemas. Depois, é realizada uma inferência bayesiana nesses dados através de uma cadeia MCMC para determinar a distribuição de probabilidades dos parâmetros livres. Entre esses parâmetros está a constante de Hubble que desejamos estimar. 


## Project 03.a - Deep or Bayesian? SL parameter inference 

(João)

### Introduction
The gravitational lensing effect, first proposed by Albert Einstein and confirmed later, in the XX century, has been a powerful tool in astronomy and cosmology. This is due to its slip parameter (also called by gamma factor), which gives an intuition on how different a theory could be from general relativity. In addition, with new surveys, such as, the last release of the dark energy survey (DES), the Hyper Suprime-Cam and the first available data of the Large Synoptic Survey Telescope (LSST) we will be able to improve precision. For this reason, faster and automated methods will be required in order to analyse these data. In this work, we intend to do a cross-check analysis between deep learning and Bayesian approaches.
### Goal
Our goal is to model a few strong lensing systems using a Bayesian regression and compare parameters obtained by a deep learning approach according to https://arxiv.org/abs/1911.06341. As a result, we are going to inspect the convergence of such MCMC algorithm and the predicted image model, as a product of an MCMC chain. Therefore, we will be able to compare the confidence levels and obtain the usual statistics, such as standard deviation, in order to realize a 2nd level validation on the sample.
### What am I going to do?
First, we are going to inspect the provided data, identifying training, validation and test dataset as well as the corresponding noise-map images. We are also going to perform a Bayesian regression of a few strong lensing systems, using PyAutoLens software (https://pyautolens.readthedocs.io). As PyAutoLens uses a multi-band cutout (image combined by individual GRI bands), combining those images is going to be required. In order to analyse MCMC chains, we are going to use the usual numpy package (more precisely the numpy percentiles) and getdist, which is a software that helps to plot normalized confidence levels. In order to obtain additional information on .fits files, DS9 and SExtractor may also be useful.

## Project 04 - Cosmological MLE from a power spectrum
Matheus Vitor

### Introdução 
Grandes estruturas cósmicas como galáxias e conglomerados afetam a trajetória da luz de fontes mais distantes que se propagam em nossa direção. Assim distorcendo a imagem dessas galáxias distantes. Esse efeito é conhecido como lenteamento fraco (weak lensing) e foi observado pela primeira vez no ano 2000 no artigo https://arxiv.org/abs/1002.2136. Graças ao lenteamento fraco produzido por estruturas em larga escala temos uma forma 
independente de restringir a distribuição de matéria escura no universo, a energia escura e até mesmo restringir modelos de gravitação modificada.   
 
### Objetivo 
Obter parâmetros cosmológicos, como a densidade de matéria escura no universo e o parâmetro de Hubble, através do método de máxima verossimilhança aplicado a um modelo teórico de espectro de potência em comparação a espectros de potência obtidos através da análise de mapas de cisalhamento (cosmic shear) observados.  

### Metodologia 
Primeiramente preciso definir um modelo teórico para o espectro de potência da matéria em função dos parâmetros cosmológicos e dos dados obtidos pelos mapas de cisalhamento. Então aplicar o método de máxima verossimilhança e obter os melhores valores dos parâmetros cosmológicos dado um conjunto de mapas de cisalhamento. 

### Referências
Schneider P. (2006) Weak Gravitational Lensing. In: Gravitational Lensing: Strong, Weak and Micro. 
https://arxiv.org/pdf/astro-ph/0003008.pdf
https://arxiv.org/pdf/1302.0183.pdf

## Project 05 -  Clustering analysis to separate star/galaxies in a survey.
Thiago Carneiro
### GOAL

Correctly distinguish between stars and galaxies in a catalog using a variety of machine learning techniques.

### INTRODUCTION
Surveys map astronomical numbers of both stars and galaxies (among others) on their catalogues. Stars, in particular, aren't of interest to many cosmological analysis. However, their visual aspect can be mistaken for an elliptical galaxy. Considering the rapidly growing rate at which new data is being acquired, we need to be able to automatically sift stars from other celestial bodies in such catalogues with confidence.

### WHAT AM I GOING TO DO?
I'll approach the problem of identifying stars in a catalog using multiple ML techniques (e.g. Random Forest Trees, Logistic Regression, etc.), measuring how well each approach partitions the data. The results will allow us to evaluate which methods are the best ones for this task.

## Project 06 - We don't really miss you 
Cristiane

### Introduction

The light we detect from the galaxies we observe is affected by the expansion of the universe, which causes its electromagnetic spectrum to redshift. To estimate the spectral redshift we use emission lines from known elements, such as hydrogen and iron. We compare those line’s wavelengths emitted by the galaxy to the wavelengths emitted  by an object at rest, thus the redshift is z = (𝝀-𝝀0)/𝝀0. However, this procedure is not practical to use in large volumes of data, becoming a problem to the astrophysicists nowadays. A different technique uses photometry to estimate the redshift: you can compare the brightness of a galaxy viewed through various standard filters to ready-made templates that represent a galaxy at various redshifts, and one can check which template fits better. Another way is to employ supervised machine learning techniques to create models that are able to predict the values of the redshifts based only on photometric measures. It seems necessary to point out that despite the clear practical advantage, these methods are not so precise as the spectroscopic way to determine the redshift, and besides, there is the fact that missing data can affect the results and influence the error in prediction.

### Goal

Our goal is to evaluate the effectiveness of different machine learning techniques in predic the photometric redshift incorporating missing data approaches to the input data used to train and test the models, studying its effects on the predictive models generated. One of the prospects is to find the relative importance of each band in the final prediction of the inferred photometric redshift. 



### What am I going to do?

We will use machine learning techniques such as random forest, dense neural network and LightGBM to build our models. First, to train the models we will calculate the limit in the magnitude for each band in the survey, and remove all data that has one or more missing values, and choose then a set of parameters (bands) to use, such as G, R, I, Z, W1, W2. Then, we choose one band at a time to exclude from the data and infer the quality of the predictions. Finally, now we test again with all the initial bands, but we choose a band at a time and use 50% of the data, filling the other 50% with missing data techniques. One kind of missing data technique is to utilize the mean of the neighboring bands. Other kind is the Copula Imputation.


## Project 07 - Where is Waldo? 
Maurício
### Introduction
Outliers in datasets are dubious figures: they can, in regression or classification processes, result in poor fit and poor predictive power for the model. But, in the realm of astronomy, an outlier can mean a rare object or even a phenomenon never before detected!

### Goal
Use outlier detection techniques to spot rare objects, like merging galaxies, irregular ones and maybe an unicorn!
First of all, we need to know how to detect and isolate these exceptional elements. Outlier automatic detection methods can be used during the modeling pipeline, like any other data preparation transformation that will be applied to the dataset. At the end of this project, we should provide automatic detection models for outliers as alternative methods to statistical techniques, and that support a large number of input variables that present complex and unknown interrelationships.

### Methodology
The Python scikit-learn library features a good number of built-in automatic methods for identifying outliers in datasets: each of these methods has a slightly different definition of outliers, which gives us the possibility to compare the final results and obtain a redundancy effect. There are four methods we will use to detect outliers (further discussions about them will be made during the presentation, but they are listed in the bibliography section):
1. Isolation Forest;
2. Minimum Covariance Determinant;
3. Local Outlier Factor;
4. One-Class SVM [support vector machine].
After selecting our targets, from a dataset suggested by the professor and duly pre-processed, we will use the tools seen in class to create images of these outliers that will be analyzed: what will we find?

### References

Bernhard Schölkopf, John C. Platt, John C. Shawe-Taylor, Alex J. Smola, and Robert C. Williamson. 2001. "Estimating the Support of a High-Dimensional Distribution." Neural Comput. 13, 7 (July 2001), 1443–1471. DOI:https://doi.org/10.1162/089976601750264965

F. T. Liu, K. M. Ting and Z. Zhou, "Isolation Forest." 2008 Eighth IEEE International Conference on Data Mining, 2008, pp. 413-422, doi: 10.1109/ICDM.2008.17.

Hubert, Mia, Michiel Debruyne, and Peter J. Rousseeuw. "Minimum covariance determinant and extensions." Wiley Interdisciplinary Reviews: Computational Statistics 10.3 (2018): e1421.

Markus M. Breunig, Hans-Peter Kriegel, Raymond T. Ng, and Jörg Sander. "LOF: identifying density-based local outliers." Proceedings of the 2000 ACM SIGMOD international conference on Management of data (SIGMOD '00). Association for Computing Machinery, New York, NY, USA, 2000, 93–104. DOI:https://doi.org/10.1145/342009.335388

https://machinelearningmastery.com/model-based-outlier-detection-and-removal-in-python/


## Project 08 - Searching for pattern in galaxy structure 
Mariana
 É conhecido por meio de observações que o ambiente tem papel relevante nas propriedades das galáxias (por exemplo, Dressler et al 1980). No entanto, ainda não sabemos de que forma o ambiente interfere na evolução intrínseca das galáxias. Para obter insights sobre este tema podemos investigar aglomerados de galáxias, que são as estruturas mais densas do Universo, em seus estágios iniciais de formação - os chamados protoaglomerados. Ao analisarmos protoaglomerados em diferentes estágios evolutivos podemos ter pistas sobre a evolução do efeito ambiental nestas estruturas muito massivas.	Neste projeto buscamos refazer a análise de Toshikawa et al 2020 em z aproximadamente 4 , em que um dos argumentos* para sugerir a existência de protoaglomerados é: se a distribuição espacial das galáxias dentro de um volume amostrado tem baixíssima probabilidade de ser randômica, estas galáxias provavelmente estão agrupadas por alguma razão física (poço de potencial gravitacional) invés de constituirem uma estrutura formada ao acaso. Neste caso há indícios da existência de um protoaglomerado. Vamos verificar se um dos protoaglomerados identificados no artigo Toshikawa et al 2020 é provavelmente uma estrutura formada ao acaso ou não. Para fazer esta análise vamos utilizar os dados do próprio artigo sobre um protoaglomerado de 13 galáxias em z~4 identificado por eles e:
* Redistribuir randomicamente todas as galáxias detectadas dentro do volume amostrado por eles
* Verificar a probabilidade de 13 do número total de galáxias se agruparem dentro de uma faixa de redshift de deltaz=0.02 (como no protoaglomerado detectado)
* Concluir se esta estrutura de 13 galáxias dentro de um deltaz=0.02 tem alta ou baixa probabilidade de ser uma estrutura formada ao acaso e comparar com os resultados de Toshikawa et al 2020
Existem outros argumentos como tamanhos característicos de protoaglomerados em z~4 e cálculo de sobredensidade de galáxias na região, mas o foco deste projeto é apenas na probabilidade de se encontrar uma determinada distribuição espacial de objetos

### Objetivo
-Detectar estruturas em formação, como aglomerados de galáxias em alto redshift


### Next Steps

-Em um futuro próximo estender a análise para galáxias detectadas por fotometria em banda estreita em z~4.5


### Referências:
Dressler, A. 1980, ApJ, 236, 351-365
Toshikawa, J., Malkan, M. A., Kashikawa, N., et al. 2020, ApJ, 888, 89, doi: 10.3847/1538-4357/ab5e85 


## Project 09 - Bayesian analysis of velocity dispersion expression with modified gravity 
Fernanda
### Introduction

Strong lensing is an important tool to determine constraints on the Post-Newtonian Parameter  (https://arxiv.org/abs/1701.00357). It can be used to test gravitational models, like Einstein’s General Relativity or f(R) theories. One way to test modified gravity is including new terms on the velocity dispersion expression (https://arxiv.org/abs/2011.15089), a parameter that can be measured with spectroscopic observations and its expression depends on . That’s why its expression is so important because using it we can determine the value of the Post-Newtonian Parameter.

### Goal

Bayesian analysis is used to minimize theoretical functions. So, here our goal is to minimize our new velocity dispersion expression to obtain the value which maximizes our distribution.


## Project 10 - Estimating stellar metallicities with S-PLUS photometry 
Eduardo
### Introduction
Traditionally, one may refer to stellar metallicity as a comparative quantity that works as a first approach to understanding the chemical composition of stars.The amount of iron (relative to hydrogen) of a star is denoted [Fe/H], where the brackets indicate a comparison against the Sun, and it approximately accounts for all elements other than hydrogen and helium present in its atmosphere. Metallicity values are usually estimated by means of spectroscopy, given that atomic transitions leave unique signatures on stellar spectra, but photometry can also be explored, especially if various broad and narrow band filters are available, as it is the case for the Southern Photometric Local Universe Survey (S-PLUS).
### Goal
With a set of 7 narrow-band filters along with 5 broad-band filters, S-PLUS provides information on sensitive regions of the spectrum that allow for consistent estimations of stellar metallicities. My goal is to estimate photometric metallicities focusing on metal-poor stars, since these Milky Way’s relics can give important information on the Galaxy formation and evolution.
### What am I going to do?
I am going to select stars from the S-PLUS DR2 with good photometry and search for their spectroscopic metallicities in various available surveys in literature. With these data, I’ll use LightGBM, a gradient-boosting python library, to estimate metallicities using information from S-PLUS filters.

## Project 11 - Classification of astronomical objects from their light curves using ML (Luigi)
### INTRODUCTION 
In astronomical observations, many astronomical objects with variable brightness can be found. However, the corresponding light curves (the curve representing brightness variation over time) are different for distinct classes of objects. It is possible to use this fact to classify those objects, identifying the differences in their light curves and assigning the correct classes to each kind of curve. 
GOAL
Use a Machine Learning model to classify a set of astronomical objects with variable brightness from their light curves.
### INTENDED STEPS
   * Get the data from PLAsTiCC Astronomical Classification, available in kaggle.com, inspect it and understand the meaning of each data.
   * The model intended to be used is Random Forest, because of its relative simplicity and comprehensiveness, which will increase the chances of completing the work on time.
   * Try to understand which features could be obtained from the time series data referring to light curves, then organize those features and use them in the model.
   * Use the Random Forest algorithm, and use MAE to have an idea of the precision of the model.
   * If there's time, compare those results with another simpler model, the Decision Tree, comparing their MAE.

## Project 12 - Seismic facies analysis using machine learning. (Eldues)
### INTRODUCTION
Seismic reflection data are a key source of information in numerous fields of geoscience, including sedimentology and stratigraphy (e.g., Vail, 1987; Posamentier, 2004), structural geology (Baudon and Cartwright, 2008; Jackson et al., 2014), geomorphology (e.g., Posamentier and Kolla, 2003; Cartwright and Huuse, 2005; Bull et al., 2009), and volcanology (e.g., Hansen et al., 2004; Planke et al., 2005; Magee et al., 2013). However, the often subjective and nonunique interpretation of seismic reflection data has led to longstanding debates based on contrasting geologic interpretations of the same or similar data sets (e.g., Stewart and Allen, 2002; Underhill, 2004). Moreover, seismic interpretations require significant amounts of time, experience, and expertise from interpreters (e.g., Bond et al., 2012; Bond, 2015; Macrae et al., 2016). We believe that machine-learning techniques can help interpreters reduce some of these problems associated with seismic facies analyses.
https://library.seg.org/doi/full/10.1190/geo2017-0595.1#pane-pcw-references
## GOAL
Implement tools and libraries used in class.


## Project 13 - Estimating the Photometric Redshift.


### Introduction:
The traditional method to estimate the redshift of some object concerns observing its spectrum (the distribution of luminosity energy emitted to each frequency), and identifying the lines of absorption and emission displaced because of the relative velocity between the source and observer. Although this method works very well, to observe the complete spectrum of any object takes so much time, which encourages us to look for alternative ways (more efficiently) to estimate the redshift of objects in the sky.
One possibility is to infer some relation between the real redshift and magnitudes measured in some photometric bands. The output result from this is called photometric redshift. Then, following this way, it is not necessary to measure the entire spectrum.




### Goal
The goal is to use  machine learning (ML) methods to deal with big dataset (magnitudes measured in many photometric bands) to estimate the redshift of the objects, what we call the photometric redshift. A important characteristic of this kind of dataset is the missing values in some photometric bands, and so we investigate what is the better way to deal with this trouble, which may be inputting statistical representative values of magnitudes in the missing ones or eliminating these objects of the analysis (although  this decrease the dataset).  Also, it is interesting to verify how much each photometric band influences the final predictions of ML, mainly it concerns bands W1, W2, W3, W4 in the catalog, once they present the most number of  missing values.



### What am I going to do?

Firstable i intend to determine if the information from the photometric bands W1, w2, w3, w4 really matters to determine a reliable photometric redshift. To do this, I clean the catalog, throwing away all the objects with some missing value (for any magnitude). Then I apply some Deep Learning routines using tensorflow to this "cleaned dataset". Also, I repeat the method not using some photometric bands, and comparer the final predictions. After that, I wish to apply the same routine in the original dataset but changing the missing data for representative values of their statistical distribution. Finally I will compare how much this input fake data can improve (or not) the final predictions of our Deep Learning model.

## Project 14 - Bayesian Inference using Normalizing Flows

### Introdução

Lentes Gravitacionais são um fenômeno que consiste no desvio da luz emitida por uma fonte até chegar ao observador devido à presença de um corpo massivo no caminho, como um cluster de galáxias. Entre os fenômenos mais peculiares associados às lentes gravitacionais, há o chamado Anel de Einstein, quando a luz pontual da fonte é deformada em um anel ao redor da lente gravitacional, que está alinhada entre a fonte e o observador. Neste trabalho, pretende-se obter estimativas para variáveis associadas ao fenômeno das lentes gravitacionais através de inferência Bayesiana utilizando a técnica conhecida como Normalizing Flows.

### Objetivo

Estimar o Raio de Einstein, a dispersão de velocidades e os redshifts da fonte e da lente de um dataset de lentes gravitacionais usando inferência Bayesiana através de técnicas de Normalizing Flows para simular distribuições de probabilidades.

### Método

Normalizing Flows é um conjunto de transformações paramétricas diferenciáveis e invertíveis que convertem distribuições simples, como a Distribuição Normal, em aproximações de qualquer outra distribuição. Usando uma rede neural para aprender os parâmetros dessas transformações, é possível obter boas aproximações de distribuições a partir de dados pré-existentes. Finalmente, faz-se um sample a partir da distribuição final obtida e calcula-se as variáveis desejadas a partir destes dados simulados. 

Esse método será utilizado para obter o Raio de Einstein, a dispersão de velocidades e os redshifts da fonte e da lente de um dataset de imagens de lentes gravitacionais.
