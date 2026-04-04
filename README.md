#  Estimation du traffic routier

##  Objectifs

L’objectif de ce projet est de mettre en place un modele de machine learning pour estimer l’évolution du trafic routier dans chaque jonction d’un carrefour étant donné que la pression sur les infrastructures des villes ne fait qu’augmenter d’année en année. Dans ce projet nous considérons les données obtenues des capteurs dans un carrefour constitué de 4 jonctions pour la modélisation.  

---

##  Methode

Etant donné que les données obtenues sont des données des capteurs enregistrés par heures à chaque jonction, nous avons choisi deux types de modèles notamment les Long Short Term Memory (LSTM) et les Gated Recurrent Unit (GRU) qui sont une option simplifiée des modèles LSTM. Notre modelisation se focalise sur la jonction 1. Pour modeliser le trafic dans les autres jonctions il suffit de changer seulement deux variable dans le notebook. La premiere est le type de jonction (*type_jonction*) et la variable *interval* dans la fonction *Difference*. En efft cette fonction est utiliser afin d'extraire l'effet de la saiaonalité. Donc cette variable devrait etre adapté en fonction de la nature des données. 

---

##  Resultats
 Les résultats sont présentés dans le dossier `Images/`:

 - ![Distribution du nombre de vehicules par type de jonction](D:\DOCUMENTS\PROJETS\Estimation-du-traffic-routier---ATUT2025\Images\Distribution du nombre de vehicules par type de jonction.png)
 Ce fichier présente la distribution (histogramme) du nombre de véhicules par type de jonction

 - ![Evolution de la fonction de perte du modèle LSTM](D:\DOCUMENTS\PROJETS\Estimation-du-traffic-routier---ATUT2025\Images\Evolution de la fonction de perte du modèle LSTM.png)
 Cette image illustre l'évolution de la fonction de perte du modèle LSTM sur les données d'entrainement et de test.

  - ![Evolution de la fonction de perte du modèle GRU](D:\DOCUMENTS\PROJETS\Estimation-du-traffic-routier---ATUT2025\Images\Evolution de la fonction de perte du modèle GRU.png)
 Cette image illustre l'évolution de la fonction de perte du modèle GRU sur les données d'entrainement et de test.

  - ![Valeurs prédites par le modèle LSTM](D:\DOCUMENTS\PROJETS\Estimation-du-traffic-routier---ATUT2025\Images\Valeurs prédites par le modèle LSTM.png)
 Cet graphique montre l'évolution des prédictions du modèle LSTM ainsi que les valeurs réelles du trafic routier.

   - ![Valeurs prédites par le modèle GRU](D:\DOCUMENTS\PROJETS\Estimation-du-traffic-routier---ATUT2025\Images\Valeurs prédites par le modèle GRU.png)
 Cet graphique montre l'évolution des prédictions du modèle GRU ainsi que les valeurs réelles du trafic routier.

Les résultats sont présentés dans les différents graphique y joins à ce notebook. Ils indiquent plutôt de bonnes performances dans la modélisation de nos données et la prédiction.
---

## 📂 Contenu du repository
- **notebook.ipynb** : `Estimation-du-traffic-routier---ATUT2025` –ensemble des étapes liées à au dévéloppement des modèles.  
- **data** : `dossier qui contient les données utlisées pour la modélisation`.   
- **README.md** : `Le fichier readme qui contient l'ensemble des informations sur le projet`.  
- **gitignore** : `Un fichier qui permet d'ignorer certains fichiers non important pour le cloning/` .    
- **Images** : 'Dossiers qui contient le images sur les résultats de nos modélisations.

---

##  Limites

En guise de limite on note que les données ne sont pas adaptées au contexte du Togo car les données dans le cas de ce pays n’existent pas. Une autre limite est la non prise en compte des données météorologique. En effet, les données météo correspondant ne sont pas trouvable. Une future amélioration pourrait être de tenir en compte ces données pour améliorer les performances des modèles car il est naturel que l’évolution du trafic routier soit liée à l’état de la météo. Par ailleurs il est à noter que la simplicité du modèle est liée au fait que son entrainement a été fait en local.  

---