# Python_DS
🐍🐍

**Couverture temporelle des tables**
Effectifs.cvs : 31/12/2015 à 31/12/2021
Base_pollution.csv : 2016


**Variables de la table effectifs.csv :**

annee [date], cla_age_5 [text] (classe d’âge par tranche de 5 ans), sexe [text], region [text], dept [text] (département), libelle_classe_age [text] (libellé de la classe d’âge), libelle_sexe [text] (libellé du sexe)

Et :
* patho_niv1: [text] groupe de pathologies (ou traitements chroniques ou épisodes de soins)
* patho_niv2: [text] sous-groupe de pathologies (ou traitements chroniques ou épisodes de soins)
* patho_niv3: [text] sous-groupe détaillé de pathologies (ou traitements chroniques ou épisodes de soins)
* top: [text] libellé technique de la pathologie (ou traitement chronique ou épisode de soins)
* Ntop: [int] effectif de patients pris en charge pour la pathologie (ou traitement chronique ou épisode de soins) dont il est question
* Npop: [int] population de référence qui est celle de la cartographie des pathologies et des dépenses de l’Assurance Maladie
* prev: [double] prévalence de patients pris en charge pour la pathologie (ou traitement chronique ou épisode de soins) dont il est question
* Niveau prioritaire [text]
* tri [double]


**Variables de la table base_pollution.csv :**
Les variables de la  table sont celles utilisées pour calculer le potentiel ou pouvoir de réchauffement global (PRG). C'est un indicateur qui vise à regrouper sous une seule valeur l'effet additionné de toutes les substances contribuant à l'accroissement de l'effet de serre (définition de l'INSEE).
Les variables recouvrent les principales activités humaines à l'origine de la pollution atmosphérique.

***!!!! Les unités des chiffres de la table sont introuvables !!!!***

Nous croisons cette base avec notre base principale car la qualité de l'air a des conséquences non négligeables sur la santé des agents. En effet, la pollution de l’air provoque à elle seule près de 6,5 millions de décès chaque année, soit un décès sur huit, ce qui la positionne parmi les principaux risques pour la santé dans le monde (source : https://www.atmo-france.org).
Lien pour des chiffres clés sympas : https://www.atmo-france.org/article/chiffres-cles

**Description de la table base_pollution.csv :**

Le Ministère en charge de l’Environnement a chargé le Centre Interprofessionnel Technique d’Etudes de la Pollution Atmosphérique (CITEPA) d’une mission de « territorialisation » – ou « spatialisation » - de l’_inventaire national de GES_. La résolution spatiale est communale, structures stables dans le temps et ensuite agrégeables par EPCI.

Il est établi à partir à la fois à partir d’une décomposition des émissions nationales de GES au niveau communal et d’informations déjà spatialisées.

Cet inventaire spatialisé a vocation à donner des ordres de grandeur pertinents pour l’année 2016. Il n’a pas le niveau de finesse et de précision des travaux d’inventaire réalisés au niveau territorial par les associations agréées de surveillance de la qualité de l’air (www.atmo-france.org), les agences régionales de l’énergie (www.rare.fr), ou des travaux nationaux à hautes résolutions spatiales et temporelles (projet de grande ampleur type Inventaire National Spatialisé - INS).


Code INSEE des régions françaises :
84 : Auvergne-Rhône-Alpes
32 : Hauts-de-France
93 : Provence-Alpes-Côte d'Azur
44 : Grand Est
76 : Normandie
28 : Centre-Val de Loire
75 : Nouvelle-Aquitaine
24 : Occitanie
27 : Bourgogne-Franche-Comté
53 : Bretagne
94 : Corse
52 : Pays de la Loire
11 : Île-de-France

Carto faite, il faut corriger les effets de taille (parce que là on a juste plein de gens dans les départements les plus peuplés), 
trouver une base avec peut-être degré d'urbanisation
trouver une solution pour temps de calcul et possibilité de clustering

COTE ENZO :
l'idée c'était de reprendre la base adaptée utilisée pour la carto pour faire des stats desc sur les maladies repiratoires 
(semble intéressant car on peut essayer de faire des liens avec l'habitat etc) 
mais en fin de sessions le résultat est "surprenant" puisque j'ai la même valeur de maladie respiratoire pour toute les catégories d'âge 
donc la suite c'est de cherhcer d'ou vient l'erreur 
si ca marche on pourra plus ou moins recopier-coller le modele de code pour faire des histogrammes en boucle je pense 

