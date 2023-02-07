# FRACASSO_MORVAN_AVC_dossier

#  I. Introduction




# II. Analyse exploratoire
## II.1. Variable dépendante 
## II.2. Variable explicatives
### II.2.A. Analyse univariée
### II.2.B. Analyse bivariée
## II.3. Types de variables

# III. Préparation de la base de données
## III.1. Nettoyage des données
### III.1.A. Valeurs manquantes
### III.1.B. Points atypiques
### III.1.C. Dichotomisation
## III.2. Sélection des variables
### III.2.A. Tests entre Stroke et les variables explicatives
#### III.2.A.1. Variables quantitatives
#### III.2.A.2. Variables qualitatives
### III.2.B. Tests entre les variables explicatives 
#### III.2.B.1. Variables qualitatives
#### III.2.B.2. Variables quantitatives
## III.3. Standardisation

# IV. Modélisation
## IV.1. SVM

`X_train_sc=pd.DataFrame(X_train_sc2)`

`X_test_sc=pd.DataFrame(X_test_sc2)`

`#Regression logistique`
`lgr = LogisticRegression( random_state=0)`
`lgr.fit(X_train_sc, y_train)`
`y_pred_lgr=lgr.predict(X_test_sc)`

`#Linear SVM`
`l_SVC = LinearSVC(random_state=0, max_iter=2000)`
`l_SVC.fit(X_train_sc, y_train)`
`y_pred_lsvc=l_SVC.predict(X_test_sc)`

`#la différence entre linear svc et svc avec kernel linear c'est qu'ils n'utilisent pas la même fonction de perte`
`#SVM avec kernel lineaire`
`svc = SVC(kernel='linear',random_state=0)`
`svc.fit(X_train_sc,y_train)`
`y_pred_svc=svc.predict(X_test_sc)`

`#SVM avec kernel rbf`
`svc_rbf = SVC(kernel='rbf',random_state=0)`
`svc_rbf.fit(X_train_sc,y_train)`
`y_pred_svc_rbf=svc_rbf.predict(X_test_sc)`

`#SVM avec kernel poly`
`svc_poly = SVC(kernel='poly',random_state=0)`
`svc_poly.fit(X_train_sc,y_train)`
`y_pred_svc_poly=svc_poly.predict(X_test_sc)`

`#SGD classifier`
`sgdc_svm = SGDClassifier(loss='hinge' ,random_state=0)`
`sgdc_svm.fit(X_train_sc, y_train)`
`y_pred_sgd=sgdc_svm.predict(X_test_sc)`




## IV.2. Réseau de neuronnes 

# V. Conclusion 


