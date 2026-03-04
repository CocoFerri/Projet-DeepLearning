# 🎧 Projet Deep Learning – Classification de Fichiers Audio

Ce dépôt contient le code et les ressources associées à notre projet de Deep Learning portant sur la **classification automatique de fichiers audio** à l’aide d’un modèle Transformer basé sur RoBERTa.

---

## 🎯 Objectif

L’objectif de ce projet est de développer un système capable de :

- 🎙 Traiter des fichiers audio (.wav)
- 📝 Transcrire l’audio en texte (via Whisper)
- 🤖 Classifier automatiquement le contenu dans différentes catégories
- 📊 Évaluer les performances du modèle

---

## 📁 Contenu du dépôt

- `Projet_DeepLearning.ipynb` : Notebook contenant :
  - Prétraitement des données
  - Entraînement du modèle
  - Évaluation
  - Tests
- `README.md` : Description du projet

⚠️ Le dataset n’est pas inclus dans ce dépôt en raison de sa taille. Il est stocké sur Google Drive.

---

## 📊 Dataset

- Environ 1000 fichiers audio au format `.wav`
- Un fichier CSV associé contenant :
  - Nom du fichier
  - Label de classification

Le CSV permet d’associer chaque fichier audio à sa classe cible.

📂 Accès au dataset :  
👉 [Lien Google Drive](https://drive.google.com/drive/folders/14dzJeyRPA2-iOVse7mg0_E-wzWf3zeCC?usp=sharing)

---

## ⚙️ Pipeline du projet

### 1️⃣ Chargement des données
- Montage du Google Drive
- Lecture des fichiers `.wav`
- Chargement du fichier `.csv`

### 2️⃣ Prétraitement
- Nettoyage des données
- Tokenisation des textes
- Encodage des labels

### 3️⃣ Modélisation
- Chargement d’un modèle RoBERTa pré-entraîné
- Fine-tuning sur notre dataset audio/textuel

### 4️⃣ Entraînement
- Optimisation avec PyTorch
- Utilisation du GPU (CUDA 11.8)

### 5️⃣ Évaluation
- Accuracy
- Loss
- Analyse des performances sur jeu de test

### 6️⃣ Test final
- Détection et transcription de ce que l'on dit
- Affichage de la classe prédite et de la probabilité associée

---

## 🧪 Tests

Le modèle peut être testé :

- En utilisant un fichier audio en format .wav
- En mode micro (Google Colab, enregistrement direct navigateur)

---

## 📈 Résultats

Le modèle atteint :

- ✅ 95% de précision sur le jeu de test

Les performances ont été évaluées avec :

- Accuracy
- Loss
- Softmax probabilities

---

## 🚀 Exécution du projet

1. Ouvrir `Projet_DeepLearning.ipynb` dans Google Colab
2. Monter Google Drive
3. Vérifier les chemins d’accès au dataset
4. Exécuter les cellules dans l’ordre
5. Pour la dernière parler une fois la cellule lancée.

---

## 🛠️ Technologies utilisées

- Python
- PyTorch
- HuggingFace Transformers (RoBERTa)
- OpenAI Whisper
- Librosa
- Jupyter Notebook
- Google Colab

---

## 🔧 Installation des dépendances

Projet développé sur Google Colab avec GPU CUDA 11.8.

### Installation principale

```bash
pip install -U transformers datasets evaluate accelerate openai-whisper
