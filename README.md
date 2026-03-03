# Projet Deep Learning – Classification de fichiers audio

Ce dépôt contient le code et les ressources associées à notre projet de Deep Learning portant sur la classification de fichiers audio à l’aide d’un modèle basé sur RoBERTa.

## 🎯 Objectif

L’objectif de ce projet est de développer un modèle capable de classifier automatiquement des fichiers audio en différentes catégories à l’aide d’un modèle Transformer (RoBERTa).

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
`Test1.wav`, `Test2.wav`, ...
Le modèle retourne la classe prédite pour chaque fichier audio testé.

## 🚀 Exécution du projet

1. Ouvrir le notebook `Projet_DeepLearning.ipynb`
2. Monter le Google Drive
3. Vérifier les chemins vers le dataset
4. Exécuter les cellules dans l’ordre

## 🛠️ Technologies utilisées

- Python
- PyTorch
- Transformers (RoBERTa)
- Librosa
- Jupyter Notebook
  
## 🔧 Installation des dépendances

Le projet a été développé et testé sur **Google Colab** avec support GPU (CUDA 11.8).

Installer les bibliothèques nécessaires :

# Installation des dépendances principales
```bash
pip install -U transformers datasets evaluate accelerate openai-whisper
```

# Installation de PyTorch avec support CUDA 11.8 (GPU)
```bash
pip install --upgrade torch torchvision torchaudio \
  --index-url https://download.pytorch.org/whl/cu118
```

⚠️ L’installation CUDA est requise pour l’entraînement et l’inférence sur GPU.

## 💻 Environnement d’exécution

- Google Colab
- Python 3.10
- GPU NVIDIA (CUDA 11.8)

## 📈 Résultats

Le modèle atteint une précision de 95% sur le jeu de test.

Les performances ont été évaluées à l’aide de métriques classiques (accuracy, loss).
