#  Estimation du traffic routier

##  Objectifs

L’objectif de ce projet est de mettre en place un modele de machine learning pour estimer l’évolution du trafic routier dans chaque jonction d’un carrefour étant donné que la pression sur les infrastructures des villes ne fait qu’augmenter d’année en année. Dans ce projet nous considérons les données obtenues des capteurs dans un carrefour constitué de 4 jonctions pour la modélisation.  

---

##  Methode

Etant donné que les données obtenues sont des données des capteurs enregistrés par heures à chaque jonction, nous avons choisi deux types de modèles notamment les Long Short Term Memory (LSTM) et les Gated Recurrent Unit (GRU) qui sont une option simplifiée des modèles LSTM. Notre modelisation se focalise sur la jonction 1. Pour modeliser le trafic dans les autres jonctions il suffit de changer seulement deux variable dans le notebook. La premiere est le type de jonction (*type_jonction*) et la variable *interval* dans la fonction *Difference*. En effet, cette fonction est utiliser afin d'extraire l'effet de la saisaonalité. Donc cette variable devrait etre adapté en fonction de la nature des données pour chaque jonction. 

---

##  Resultats
 Les résultats sont présentés dans le dossier `Images/`:

 - ![Distribution du nombre de vehicules par type de jonction](https://github.com/Katchoou/Estimation-du-traffic-routier---ATUT2025/blob/09a970488978c7d4a0ecf22e39cec14a993f0c28/Images/Distribution%20du%20nombre%20de%20vehicules%20par%20type%20de%20jonction.png)
 Ce fichier présente la distribution (histogramme) du nombre de véhicules par type de jonction.

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

- **notebook.ipynb** : Regroupe l'ensemble des étapes de développement des modèles.
- **data** : Dossier contenant les jeux de données utilisés pour la modélisation.
- **README.md** : Documentation principale présentant les informations essentielles du projet.
- **gitignore** : Fichier spécifiant les éléments à exclure lors du clonage ou du versionnement.
- **Images** : Dossier stockant les visualisations des résultats de modélisation.
- **Requirements.txt** :: Liste des dépendances nécessaires pour reproduire l'environnement du projet. Il est recommandé d'utiliser un environnement virtuel avant l'installation. 

---

##  Limites

Plusieurs limites sont à relever dans cet projet. Premièrement, les données utilisées ne sont pas spécifiquement adaptées au contexte du Togo, en raison de l'indisponibilité de données locales. Deuxièmement, les variables météorologiques n'ont pas été intégrées, faute de sources accessibles, bien que l'évolution du trafic routier y soit étroitement liée.
Enfin, la simplicité du modèle actuel s'explique par les contraintes techniques d'un entraînement réalisé en local. Une amélioration future consisterait à intégrer des données climatiques et à exploiter des capacités de calcul supérieures pour affiner les performances des modèles.
---