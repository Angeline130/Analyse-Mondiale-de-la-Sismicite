# Analyse spatio-temporelle de la sismicité mondiale (1900-2023)

🎯 Problématique
Comment identifier les zones à haut risque sismique et corréler la magnitude des événements avec la profondeur des foyers au niveau mondial ?

🛠️ Architecture & technique
Source des données : Dataset exhaustif des événements sismiques mondiaux.

Outils : Power BI & DAX.

Visualisation géographique : Utilisation de Microsoft Azure Maps pour une cartographie précise des épicentres selon la magnitude.

📊 Données
Dataset global des séismes (1900–2023)
Variables : magnitude, profondeur, localisation, énergie

🔍 Réalisations
Nettoyage et structuration des données sismiques
Création de mesures DAX pour l’analyse :
énergie totale libérée
magnitude moyenne
Conception d’un dashboard interactif Power BI
Intégration d’une carte dynamique avec Azure Maps
Mise en place d’un Play Axis pour analyse temporelle

🔢 Focus DAX & Statistiques
Pour ce projet, l'accent est mis sur les mesures physiques et les agrégations temporelles :

Extrait de code
-- Calcul de l'énergie totale libérée (en Petajoules)
```dax
Total Energie (PJ) = SUM(Earthquakes[Energy_PJ])
```
-- Magnitude Moyenne par période
```
Magnitude Moyenne = AVERAGE(Earthquakes[Magnitude])
```
Insight technique : Mise en place d'un Play Axis pour visualiser dynamiquement l'évolution des séismes année après année.

💡 Analyses et Insights
Corrélation Magnitude/Profondeur : Analyse démontrant la répartition des séismes puissants (Magnitude > 7) souvent localisés sur les ceintures de feu.

Énergie Libérée : Visualisation de l'énergie cumulée (ex: 14,50K PJ) permettant d'identifier les années de ruptures majeures.

UX Design : Utilisation d'un thème sombre (Dark Mode) pour faire ressortir les points de chaleur (Heatmap) et les zones d'impact.

📊 Aperçu du Dashboard

1. Page principale
   
<img width="1077" height="606" alt="image" src="https://github.com/user-attachments/assets/270e8877-7116-4a6d-a67b-40bc5b1c9d56" />

Focus Interactivité :

Info-bulles (Tooltips) contextuelles : Le survol de la carte et des graphiques pays déclenche des visualisations de détails (relation Énergie/Magnitude et répartition par pays), permettant une analyse granulaire sans charger le visuel principal.

Navigation intuitive : Utilisation de boutons de navigation pour séparer l'analyse globale de l'analyse temporelle dynamique (1995-2023).

Cliquer sur le bouton "Visualisation des séismes dans le monde au cours des années" améne à la page suivante :

<img width="1072" height="608" alt="image" src="https://github.com/user-attachments/assets/1e7314af-8051-4d8c-a28e-6b0454e95f8a" />

Cette page permet de visualiser le nombre de séismes et leurs emplacements de 1995 à 2023


