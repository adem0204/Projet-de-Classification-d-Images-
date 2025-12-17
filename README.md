👶🧑👴 Child / Adult / Elderly Image Classification
📄 Description

Ce projet Data Science a pour objectif de classer des images de personnes en trois catégories :

👶 Child (Enfant)

🧑 Adult (Adulte)

👴 Elderly (Âgé)

Le projet illustre un pipeline complet de data science : prétraitement des images, extraction de caractéristiques, entraînement de modèles classiques et évaluation des performances.

🗂️ Dataset

Source : Child / Adult / Elderly Classification Dataset - Roboflow

Format : YOLO (coordonnées de chaque personne dans l’image)

Licence : usage éducatif libre

Remarque : Le dataset brut contenait des images mélangées avec plusieurs personnes. Un script a été utilisé pour découper (crop) chaque personne et organiser les images par classe (child, adult, elderly) ✅.

🛠️ Prétraitement

🔹 Redimensionnement des images à 128x128 pixels

🔹 Conversion en grayscale

🔹 Extraction de caractéristiques avec HOG (Histogram of Oriented Gradients)

🔹 Split du dataset :

70% pour l’apprentissage

15% pour la validation

15% pour le test

🤖 Modèles entraînés

K-Nearest Neighbors (KNN)

Decision Tree (Arbre de décision)

Naive Bayes

Évaluation : Accuracy, matrices de confusion, précision, rappel, F1-score 📊.

📈 Résultats
Modèle	Accuracy
KNN	~93% 🏆
Decision Tree	~72% ⚡
Naive Bayes	~56% ❌

Analyse :

🏆 KNN : le plus performant grâce à la similarité visuelle capturée par HOG.

⚡ Decision Tree : moyen, limité par la haute dimension des features.

❌ Naive Bayes : moins performant à cause de l’hypothèse d’indépendance des features.

📂 Structure du projet
Child_Adult_Elderly_Classification/
│
├─ data/                   # Dataset original et prétraité
│   ├─ train/
│   ├─ valid/
│   └─ test/
│
├─ notebooks/              # Jupyter notebooks d’analyse et d’expérimentation
│
├─ scripts/                # Scripts Python pour le prétraitement et HOG
│
├─ results/                # Matrices de confusion, graphiques et rapports
│
└─ README.md

⚡ Comment utiliser le projet

📥 Télécharger le dataset depuis Roboflow.

✂️ Exécuter le script de prétraitement YOLO pour générer le dataset propre.

🖥️ Lancer l’extraction HOG et l’entraînement des modèles sur le dataset prétraité.

📊 Visualiser les résultats dans les notebooks ou le dossier results/.

🏁 Conclusion

✅ L’approche HOG + KNN offre les meilleures performances pour ce problème spécifique.

🔧 Le prétraitement est crucial pour nettoyer le dataset et obtenir un modèle fiable.

🌟 Perspectives : utiliser des CNN pour de meilleures performances et généralisation, tester d’autres descripteurs comme LBP ou SIFT.
