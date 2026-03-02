# Projet Deep Learning – Classification de fichiers audio

Ce dépôt contient le code et les ressources associées à notre projet de Deep Learning portant sur la classification de fichiers audio à l’aide d’un modèle basé sur RoBERTa.

## 📁 Contenu du dépôt

- `Projet_DeepLearning.ipynb` : Jupyter Notebook contenant l’intégralité du code du projet (prétraitement, entraînement et tests).
- `README.md` : Description du projet et du pipeline.

⚠️ Le dataset n’est pas inclus dans ce dépôt en raison de sa taille. Il est stocké sur Google Drive.

## 📊 Dataset

- Environ **1000 fichiers audio** au format `.wav`
- Un fichier **CSV** associé contenant les informations nécessaires à l’apprentissage du modèle
- Le CSV est utilisé pour relier les données audio aux labels/textes exploités par le modèle

## ⚙️ Pipeline du projet

1. Chargement du dataset audio depuis Google Drive  
2. Lecture et prétraitement des fichiers `.wav`
3. Chargement du fichier `.csv` pour l’apprentissage
4. Entraînement du modèle **RoBERTa**
5. Évaluation du modèle
6. Test du modèle sur des fichiers audio nommés `TestX.wav`
7. Prédiction et affichage de la classe associée au fichier audio

## 🧪 Tests

Les tests sont réalisés à partir de fichiers audio externes nommés selon le format :
