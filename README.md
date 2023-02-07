# FRACASSO_MORVAN_AVC_dossier

#  **I. Introduction**
  En 2019 et selon l'organisation mondiale de la santé, 12.22 millions de personnes ont subit un AVC et 6.55 millions de personnes en sont décédés, faisant de ce dernier la deuxième cause de décès dans le monde. L'AVC, accident vasculaire cérébral aussi appellé ataque, apparaît lorsque la circulation sanguine est interrompue par un vaisseau sanguin bouché (AVC ishémique) ou encore un vaisseau sanguin rompu (AVC hémorragique). Les signes d'alertes sont une apparition soudaine et brutale d'une déformation de la bouche, une faiblesse d'un côté du corps ou encore des troubles de la parole. En cas d'attaque, le risque de décès est élevé et si celui-çi n'entraîne pas la mort, il peut causer des repercussions à long terme comme la perte de vue et de parole ou encore une paralysie. Selon l'INSERM, le meilleur moyen de lutter contre les AVC est la prévention dite "première" c'est-à-dire sur le dépistage et le contrôle des risques vasculaires : la pression artérielle, le niveau de cholestérol, le diabète, l'obésité, la consommation d'alcool, le tabagisme ou encore la sédentarité. 

Dans cette analyse, nous allons nous servir d'une base de données issue de Kaggle contenant 40910 observations dans l'objectif de prévoir ces accidents vasculaires cérébraux avec plusieurs facteurs d'influences. Cette base de données contient donc une variable à expliquer qui est de type binaire c'est-à-dire qu'elle prend 1 lorsque l'individu a subit un accident vasculaire cérébral et elle prend 0 lorsque cette personne n'a subit aucun accident. Nous avons également dans cette base dix variables explicatives dont trois variables quantitatives discrètes (l'âge, le taux de glucause et l'indice de masse corporelle), une variable catégorielle (la catégorie socio-professionnelle), et cinq variables binaires (l'hypertension, maladie cardiovasculaire, le fait d'être marié, la localisation, la cigarette).

# **II. Analyse exploratoire**
Afin d'augmenter nos connaissances sur les variables présentes dans la base de donnée, nous réalisons quelques statistiques descriptives. Dans un premier temps,nous commençons par faire une analyse univariée de notre variable dépendante ainsi que de nos variables explicatives. Dans un deuxième temps, afin
d'avoir un apriori sur les relations existentes entre les variables explicatives et notre variable à expliquer qualitatives, nous réalisons une analyse bivariée. 
## *II.1. Analyse univariée* 
### II.1.A. Variable dépendante

Nous commençons par faire une analyse rapide de la variable qualitative à prédire qui prend 0 lorsque l'individi ne subit pas d'arrêt cardiaque vasculaire et qui prend 1 lorsque celui-çi en subit un. Nous observons que globalement la variable dépendante semble très bien répartie puisque nous observons que l'effectif de la catégorie 1 prend 20460 observations et l'effectif de la catégorie 0 prend 20450 observations. Ceçi nous affirme que 
cette variable n'est pas déséquilibrée puisqu'il y'a autant d'effectifs dans la modalité 1 que dans la modalité 0. Nous n'allons donc pas devoir procéder par des techniques de sous ou sur échnatillonnage pour ajuster la distrbution des deux classes. Nous pouvons passer à la suite de l'analyse exploratoire en faisant quelques statistiques des variables explicatives. 

### II.1.B. Variables explicatives

Le tableau ci-dessus représente un récapitultaif des statistiques des trois variables explicatives. En effet, il rend compte du nombre total des valeurs que prennent ces variables, de leurs moyennes, médiances et écart-types. Il décrit également les valeurs minimums et maximums ainsi que leurs premiers et troisièmes quartiles. Nous pouvons explorer et analyser chaque variable indépendemment des autres: 

> **L'âge:** Nous nous intéressons d'abord à l'âge de nos individus. Nous remarquons dans un premier temps que la valeur minimum est de -9, ce qui signifie qu'une faute de frappe a été commise puisque nous devrions avoir uniquement des valeurs positives. Cette valeur devra être supprimé par la suite. Ensuite, nous observons un écart assez important entre cette valeur minimum et la valeur maximum ; l'âge maximum est de 103 ans ce qui est probable, néanmoins cette valeur peut-être également et potentiellement considéré comme atypique. Dans un deuxième temps, nous nous intéressons à la médiane et la moyenne de cette variable. La moyenne est de 51,33 tandis que la médiane est de ce qui signifie que la moyenne d'âge des individus est de 51,33 et que 50% des individus ont 52 ans. Si nous nous intéressons de plus près à l'écart entre ces deux mesures nous pouvons dire que s'il existe des valeurs atypiques, celles-çi se trouvent en-dessous de la moyenne puisque cette dernière est en-dessous de la médiane. Intéressons nous désormais aux quartiles : comme le premier quartile est de 35 et le troisième quartile de 68, nous pouvons dire que 25% des individus ont moins de 35 ans et que 75% ont moins de 68 ans. Nous pouvons supposer que plus l'âge est élevé et plus le nombre de personnes subissant un AVC est important. 

> **L'IMC(Indice de masse corporelle):** Nous nous intéressons ensuite à l'indice de masse corporelle de cette population. Comme pour l'âge, nous remarquons un écart très important entre la valeur minimum et la valeur maximum de l'IMC, en effet la valeur la plus petite est de 11,5 tandis que la valeur la plus élevée est de 92. Cette dernière valeur semble trop élevée puisque l'IMC moyen est de 30,4 et nous supposons qu'elle est anormale, nous verrons par la suite s'il faut la supprimer. Si nous nous intéressons à la moyenne et la médiane qui sont respectivement de 30,4 et de 29,4, nous pouvons dire que l'IMC moyen est de 30,4 et 50% des individus ont une indice de masse corporelle à 29,4. En regardant de plus prés cet écart, nous pouvons supposer que s'il existe des valeurs atypiques, celles-çi se trouvent au dessus de la moyenne puisque celle-çi se trouve être au-dessus de la médiane. Intéressons nous désormais aux quartiles : comme le premier quartile est de 25,9 et le troisième quartile de 34,1, nous pouvons dire que 25% des individus ont une masse corporelle de 25,9
et que 75% possèdent un indice 34,1. Nous pouvons supposer que plus l'indice de masse corporelle est élevé et plus le nombre de personnes subissant un AVC est important. 

> **Le niveau moyen de glycémie:** Nous nous intéressons dernièrement au niveau moyen de glycémie de notre base de données. Comme pour les deux variables précédentes, nous observons un écart très important entre la valeur minimum et la valeur maximum du niveau moyen de glycémie ; la valeur minimum est de 55,12 tandis que la valeur maximum est de 271,74. Si nous nous intéressons à la moyenne et la médiane qui sont respectivement de 122,07 et de 97,92, nous pouvons dire que que la moyenne du niveau moyen de glycémie est de 122,07 et que 50% possédent un niveau moyen de glycémie égale à 97,92. En regardant de plus prés cet écart, nous pouvons supposer que s'il existe des valeurs atypiques, celles-çi se trouvent au dessus de la moyenne puisque celle-çi se trouve être au-dessus de la médiane. Intéressons nous désormais aux quartiles : comme le premier quartile est de 55,12 et le troisième quartile de 167,59 nous pouvons dire que 25% possèdent un niveau moyen de glycémie de 55,12 tandis que 75% en possèdent un de 167,59. Nous supposons que plus le niveau moyen de glycémie est élevé et plus le nombre de personnes atteintes d'un AVC est élevé. 
## *II.2. Analyse bivariée*

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
