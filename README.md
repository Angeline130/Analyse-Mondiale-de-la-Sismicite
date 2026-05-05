🌍 Analyse Spatio-Temporelle de la Sismicité Mondiale (1900-2023)

🎯 Problématique

Comment transformer un dataset géophysique complexe en une interface décisionnelle intuitive permettant d'identifier instantanément l'impact énergétique des séismes et les zones de ruptures critiques à l'échelle mondiale ?

🛠️ Architecture & Technique
Source des données : Dataset exhaustif des événements sismiques mondiaux (Filtre appliqué sur les séismes significatifs, Magnitude Moyenne : 6,94).

Outils de BI : Power BI Desktop & Moteur DAX.

Visualisation Géographique : Intégration de Microsoft Azure Maps pour une cartographie dynamique des épicentres.

Design UX : Thème Dark Mode à haut contraste pour une lecture optimisée des points de chaleur (Heatmaps) et des zones d'impact.

📊 Indicateurs Clés (KPI)
Le dashboard (référence : image_e6adb6.png) met en avant des métriques de haute précision :

Volume : 984 séismes majeurs analysés.

Puissance Énergétique : 14,50K PJ (Petajoules) d'énergie totale libérée.

Corrélation de Risque : 33,03 % des événements ont généré un tsunami.

🔍 Réalisations & Insights

1. Corrélation Physique (Magnitude vs Profondeur)
L'analyse via le nuage de points démontre une absence de corrélation linéaire forte : des séismes de magnitude > 8 surviennent aussi bien à faible profondeur qu'à plus de 600 km.

2. Analyse Temporelle et Énergétique
Anomalies Historiques : Identification de deux pics majeurs en 2004 (Sumatra) et 2011 (Tōhoku) où l'énergie libérée a atteint des records.

Cyclicité : L'utilisation d'une Heatmap (Matrice) par jour et par heure confirme le caractère aléatoire de la sismicité (aucune récurrence horaire détectée).

3. Focus DAX & Modélisation
Création de mesures personnalisées pour l'analyse physique :

Extrait de code
-- Calcul de l'énergie totale libérée (en Petajoules)

Total Energie (PJ) = SUM(Earthquakes[Energy_PJ])

-- Magnitude Moyenne par période

Magnitude Moyenne = AVERAGE(Earthquakes[Magnitude])

📊 Aperçu du Dashboard
Page 1 : Analyse Globale (image_e6adb6.png)
   
<img width="1171" height="652" alt="image" src="https://github.com/user-attachments/assets/4e73329c-b4f1-4dbc-9379-2ef6702d011f" />

Navigation Contextuelle : Utilisation d'info-bulles (Tooltips) détaillant la relation Énergie/Magnitude au survol d'un pays.

Executive Summary : Intégration d'un volet d'insights textuels automatiques (ex: "63% des séismes sont de faible magnitude < 7").

Page 2 : Visualisation Dynamique (Play Axis)
Animation Temporelle : Utilisation d'un Play Axis pour visualiser l'évolution chronologique et géographique des séismes de 1995 à 2023.

Optimisation Cartographique : Visualisation des épicentres via Azure Maps, permettant de suivre la progression des secousses le long des ceintures de feu.

<img width="1072" height="608" alt="image" src="https://github.com/user-attachments/assets/1e7314af-8051-4d8c-a28e-6b0454e95f8a" />

Cette page permet de visualiser le nombre de séismes et leurs emplacements de 1995 à 2023

Projet réalisé dans le cadre d'une étude sur la data visualisation appliquée aux risques naturels.


