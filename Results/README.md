# Dossier `results`

Ce dossier contiendra les résultats finaux de l'analyse.

## Fichiers

- `metrics_summary.csv`  
  Fichier CSV qui contiendra, pour chaque condition (style × allure), les métriques suivantes :
  - `style` : type de nage (`crawl` ou `brasse`)
  - `allure` : intensité (`modere` ou `rapide`)
  - `freq_cycle_hz` : fréquence moyenne des cycles de bras (Hz)
  - `SD_T` : écart-type des intervalles inter-pics (s)
  - `CV_T` : coefficient de variation des intervalles inter-pics (SD / moyenne)
  - `amp_moyenne` : amplitude moyenne des pics d'accélération (m/s²)

- `figures.pdf`  
  Ce fichier regroupera les figures finales (signaux filtrés + pics, fréquence par condition, régularité, etc.).  
  Il sera généré à partir du notebook `main.ipynb` une fois que les données auront été traitées.

## Génération des fichiers

Les fichiers de ce dossier seront générés par la dernière partie du notebook `main.ipynb` :

1. Détection des cycles sur la norme filtrée de l'accélération.
2. Calcul des intervalles inter-pics et des métriques (fréquence, SD, CV, amplitude).
3. Construction du tableau récapitulatif `metrics_summary.csv`.
4. Export des figures dans `figures.pdf`.
