# Python_DS
🐍🐍

**Couverture temporelle des tables**
Effectifs.cvs : 31/12/2015 à 31/12/2021
Base_pollution.csv : 2016


**Variables de la table effectifs.csv :**

cla_age_5(classe d’âge par tranche de 5 ans)
Et :
* patho_niv1: groupe de pathologies (ou traitements chroniques ou épisodes de soins)
* patho_niv2: sous-groupe de pathologies (ou traitements chroniques ou épisodes de soins)
* patho_niv3: sous-groupe détaillé de pathologies (ou traitements chroniques ou épisodes de soins)
* top: libellé technique de la pathologie (ou traitement chronique ou épisode de soins)
* Ntop: effectif de patients pris en charge pour la pathologie (ou traitement chronique ou épisode de soins) dont il est question
* Npop: population de référence qui est celle de la cartographie des pathologies et des dépenses de l’Assurance Maladie
* prev: prévalence de patients pris en charge pour la pathologie (ou traitement chronique ou épisode de soins) dont il est question
* Niveau prioritaire : niveau de gravité de la maladie


**Variables de la table base_pollution.csv :**
Les variables de la  table sont celles utilisées pour calculer le potentiel ou pouvoir de réchauffement global (PRG). C'est un indicateur qui vise à regrouper sous une seule valeur l'effet additionné de toutes les substances contribuant à l'accroissement de l'effet de serre (définition de l'INSEE).
Les variables recouvrent les principales activités humaines à l'origine de la pollution atmosphérique.

***!!!! Les unités des chiffres de la table sont introuvables !!!!***

Nous croisons cette base avec notre base principale car la qualité de l'air a des conséquences non négligeables sur la santé des agents. En effet, la pollution de l’air provoque à elle seule près de 6,5 millions de décès chaque année, soit un décès sur huit, ce qui la positionne parmi les principaux risques pour la santé dans le monde (source : https://www.atmo-france.org).
Lien pour des chiffres clés sympas : https://www.atmo-france.org/article/chiffres-cles

**Description de la table base_pollution.csv :**

Le Ministère en charge de l’Environnement a chargé le Centre Interprofessionnel Technique d’Etudes de la Pollution Atmosphérique (CITEPA) d’une mission de « territorialisation » – ou « spatialisation » - de l’_inventaire national de GES_. La résolution spatiale est communale, structures stables dans le temps et ensuite agrégeables par EPCI.

Il est établi à partir à la fois d’une décomposition des émissions nationales de GES au niveau communal et d’informations déjà spatialisées.

Cet inventaire spatialisé a vocation à donner des ordres de grandeur pertinents pour l’année 2016. Il n’a pas le niveau de finesse et de précision des travaux d’inventaire réalisés au niveau territorial par les associations agréées de surveillance de la qualité de l’air (www.atmo-france.org), les agences régionales de l’énergie (www.rare.fr), ou des travaux nationaux à hautes résolutions spatiales et temporelles (projet de grande ampleur type Inventaire National Spatialisé - INS).


CODE THEO :
Carto faite, il faut corriger les effets de taille (parce que là on a juste plein de gens dans les départements les plus peuplés), 
trouver une base avec peut-être degré d'urbanisation
trouver une solution pour temps de calcul et possibilité de clustering

COTE ENZO :
l'idée c'était de reprendre la base adaptée utilisée pour la carto pour faire des stats desc sur les maladies repiratoires 
(semble intéressant car on peut essayer de faire des liens avec l'habitat etc) 
mais en fin de sessions le résultat est "surprenant" puisque j'ai la même valeur de maladie respiratoire pour toute les catégories d'âge 
donc la suite c'est de cherhcer d'ou vient l'erreur 
si ca marche on pourra plus ou moins recopier-coller le modele de code pour faire des histogrammes en boucle je pense 



POUR LA REF SOCIOLOGIQUE SUR LE RAPPORT A LA MALADIE DES CLASSES SOCIALES :

Rappeler les inégalités terrioriales d'accès à la santé. Mais au-delà de cela, il y a un aspect sociologique directement lié aux pratiques de classe.

Par pratique de classe, on entend tout d'abord la consommation sociale. Les classes populaires sont les plus grandes consommatrices de tabac et d'alcool et on plus souvent une alimentation déséquilibrée que les membres des classes supérieures. Ces facteurs les rendent plus sujettes à la contraction de maladie.

A cela s'ajoute le rapport au corps différencié entre classes sociales, étudié particulièrement par les sociologues Luc Boltanski et Pierre Bourdieu. Dans « Les usages sociaux du corps », Annales (1971), Luc Boltanski enquête sur le rapport à la maladie. Il utilise un certain nombre d’indicateurs (alimentaires, médicaux, relation à la douleur, soins corporels et de beauté…) et d’enquêtes sociales. Cela lui permet de délimiter les habitus, ou usages sociaux, corporels propres aux différentes classes sociales. Il constate que les classes populaires nouent une approche plutôt instrumentale avec leur corps et valorisent beaucoup la force physique, ce qui les conduit à une meilleure tolérance à la douleur. Les classes populaires consultent pour des motifs graves alors que les catégories supérieures ont une approche plus préventive et recourent plus spontanément aux soins de spécialistes.

Cela a une influence sur le taux de survie face à un cancer. Selon une étude de Santé publique France de 2021, "Influence de l'environnement social sur la survie des patients atteints d'un cancer en France. Étude du réseau Francim" (https://www.santepubliquefrance.fr/maladies-et-traumatismes/cancers/cancer-du-col-de-l-uterus/documents/article/influence-de-l-environnement-social-sur-la-survie-des-patients-atteints-d-un-cancer-en-france.-etude-du-reseau-francim) "l'excès de mortalité lié au cancer peut être jusqu'à deux fois supérieur chez les patients des zones les plus défavorisées par rapport aux patients des zones les moins défavorisées".


RESSOURSES INTERESSANTES POUR L'ANALYSE :

Santé publique France, 2021  : "Les résultats soulignent que les baisses ponctuelles des niveaux de pollution au printemps 2020 ont été associées à des bénéfices non-négligeables pour la santé avec environ 2 300 décès évités en lien avec une diminution de l’exposition de la population française aux particules ambiantes. "
ET "Chaque année près de 40 000 décès seraient attribuables à une exposition des personnes âgées de 30 ans et plus aux particules fines (PM2,5)."
Article dispo : https://www.santepubliquefrance.fr/presse/2021/pollution-de-l-air-ambiant-nouvelles-estimations-de-son-impact-sur-la-sante-des-francais