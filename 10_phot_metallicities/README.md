# Métodos para análise de grande volume de dados e Astroinformática - CBPF - 2021.1 - Professor Clécio de Bom

## Objetivo e dados

Este projeto é uma abordagem inicial para tentar estimar valores de metalicidades estelares utilizando a fotometria do catálogo
[S-PLUS](https://splus.cloud/)
e dados espectroscópicos de três levantamentos:
[LAMOST (DR7)](http://dr7.lamost.org/),
[GALAH (DR3)](https://www.galah-survey.org/dr3/the_catalogues/) e
[SEGUE](http://www.sdss3.org/surveys/segue2.php).
Para mais informações sobre os catálogos, consultar os links referidos.

Os parâmetros estelares utilizados foram pensados com o objetivo de maximizar o número de estrelas de tipos espectrais F, G ou K:

* 4500 < Teff < 7500

* 0 < log g < 5

* -7 < [Fe/H] < 1

Nos casos de [GALAH (DR3)](https://www.galah-survey.org/dr3/the_catalogues/) e [LAMOST (DR7)](http://dr7.lamost.org/),
os dados foram obtidos nos links citados, com as restrições de parâmetros apresentadas acima;
já para buscas de
[S-PLUS](https://github.com/cdebom/AstroStatistic2021class/files/7737668/SQL_search_SPLUS.txt)
e
[SEGUE](https://github.com/cdebom/AstroStatistic2021class/files/7737667/SQL_search_SEGUE.txt),
foram usados códigos em SQL para seleção dos dados em cada caso.

Em especial, pode ser apropriado mencionar que a obtenção de dados do S-PLUS (implementada no 
[código](https://github.com/cdebom/AstroStatistic2021class/blob/main/10_phot_metallicities/jupyter_project_final_EMP.ipynb) em Python)
leva da ordem de algumas horas para compilar por conta do grande volume de dados (~1.4 GB).
Por conveniência, consultar este [link](https://mega.nz/folder/1VR0GLIJ#TtPJ7eUO16nfHR3n9SxQGg) para download dos dados já prontos para uso.

Os [slides de apresentação](https://github.com/cdebom/AstroStatistic2021class/files/7737694/projeto_AstroBigData21_EMP.pdf)
contêm outros links úteis para obtenção dos dados.

## Método e código

Foram exploradas árvores de decisão, mais especificamente usando a técnica de [gradient boosting](https://en.wikipedia.org/wiki/Gradient_boosting),
por meio do algoritmo LightGBM. Os parâmetros utilizados podem ser consultados no
[código](https://github.com/cdebom/AstroStatistic2021class/blob/main/10_phot_metallicities/jupyter_project_final_EMP.ipynb),
que foi desenvolvido permitindo reprodutibilidade e tem outros comentários úteis. 
Para informações sobre instalação e uso do LightGBM, [ReadTheDocs](https://lightgbm.readthedocs.io/en/latest/).
Por fim, vale ressaltar que os caminhos de leitura dos dados estão baseados na máquina nativa, i.e. os endereços precisam ser adaptados em caso de reprodução.

### E-mail para contato: eduardopereira@on.br
