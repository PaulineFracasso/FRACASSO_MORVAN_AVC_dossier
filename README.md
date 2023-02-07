# FRACASSO_MORVAN_AVC_dossier

#  **I. Introduction**
  En 2019 et selon l'organisation mondiale de la santé, 12.22 millions de personnes ont subit un AVC et 6.55 millions de personnes en sont décédés, faisant de ce dernier la deuxième cause de décès dans le monde. L'AVC, accident vasculaire cérébral aussi appellé ataque, apparaît lorsque la circulation sanguine est interrompue par un vaisseau sanguin bouché (AVC ishémique) ou encore un vaisseau sanguin rompu (AVC hémorragique). Les signes d'alertes sont une apparition soudaine et brutale d'une déformation de la bouche, une faiblesse d'un côté du corps ou encore des troubles de la parole. En cas d'attaque, le risque de décès est élevé et si celui-çi n'entraîne pas la mort, il peut causer des repercussions à long terme comme la perte de vue et de parole ou encore une paralysie. Selon l'INSERM, le meilleur moyen de lutter contre les AVC est la prévention dite "première" c'est-à-dire sur le dépistage et le contrôle des risques vasculaires : la pression artérielle, le niveau de cholestérol, le diabète, l'obésité, la consommation d'alcool, le tabagisme ou encore la sédentarité. 

Dans cette analyse, nous allons nous servir d'une base de données issue de Kaggle contenant 40910 observations dans l'objectif de prévoir ces accidents vasculaires cérébraux avec plusieurs facteurs d'influences. Cette base de données contient donc une variable à expliquer qui est de type binaire c'est-à-dire qu'elle prend 1 lorsque l'individu a subit un accident vasculaire cérébral et elle prend 0 lorsque cette personne n'a subit aucun accident. Nous avons également dans cette base dix variables explicatives dont trois variables quantitatives discrètes (l'âge, le taux de glucause et l'indice de masse corporelle), une variable catégorielle (la catégorie socio-professionnelle), et cinq variables binaires (l'hypertension, maladie cardiovasculaire, le fait d'être marié, la localisation, la cigarette).

# **II. Analyse exploratoire**
Afin d'augmenter nos connaissances sur les variables présentes dans la base de donnée, nous réalisons quelques statistiques descriptives. Dans un premier temps,nous commençons par faire une analyse univariée de notre variable dépendante ainsi que de nos variables explicatives. Dans un deuxième temps, afin
d'avoir un apriori sur les relations existentes entre les variables explicatives et notre variable à expliquer qualitatives, nous réalisons une analyse bivariée. 
## *II.1. Variable dépendante* 
Nous commençons par faire une analyse rapide de la variable qualitative à prédire qui prend 0 lorsque l'individi ne subit pas d'arrêt cardiaque vasculaire et qui prend 1 lorsque celui-çi en subit un. Nous observons que globalement la variable dépendante semble très bien répartie puisque nous observons que l'effectif de la catégorie 1 prend 20460 observations et l'effectif de la catégorie 0 prend 20450 observations. Ceçi nous affirme que 
cette variable n'est pas déséquilibrée puisqu'il y'a autant d'effectifs dans la modalité 1 que dans la modalité 0. Nous n'allons donc pas devoir procéder par des techniques de sous ou sur échnatillonnage pour ajuster la distrbution des deux classes. Nous pouvons passer à la suite de l'analyse exploratoire en faisant quelques statistiques des variables explicatives. 
## *II.2. Variable explicatives*
### II.2.A. Analyse univariée
### II.2.B. Analyse bivariée
## *II.3. Types de variables*

<img width="1091" alt="Capture d’écran 2023-02-07 à 18 29 35" src="https://user-images.githubusercontent.com/118168094/217335053-80b0d207-f725-4bc2-951d-e4785330e23e.png">


# **III. Préparation de la base de données**
## *III.1. Nettoyage des données*
### III.1.A. Valeurs manquantes
### III.1.B. Points atypiques
### III.1.C. Dichotomisation
## *III.2. Sélection des variables*
### III.2.A. Tests entre Stroke et les variables explicatives
#### III.2.A.1. Variables quantitatives
#### III.2.A.2. Variables qualitatives
### III.2.B. Tests entre les variables explicatives 
#### III.2.B.1. Variables qualitatives
#### III.2.B.2. Variables quantitatives
## *III.3. Standardisation*

# **IV. Modélisation**
## *IV.1. SVM*
## *IV.2. Réseau de neuronnes* 

# **V. Conclusion**




Pour insérer des images. : 

Sur l'interface web de github, crée une issue (Issues > new issue) car sur cette interface tu peux y insérer des images (par exemple insère toutes celles qui te seront utiles dans ton readme). Une fois qu'elle est créée, tu peux faire un clic droit sur une des images et sélectionner "copier l'url de l'image"

Passe maintenant sur ton readme.md, et à l'endroit que tu veux qu'une image apparaisse, écris ceci :

![alt tag](url de ton image)

par exemple

![alt tag](https://cloud.githubusercontent.com/assets/3968618/9588666/d029268e-5029-11e5-8a0c-41ecd04207f4.png)
