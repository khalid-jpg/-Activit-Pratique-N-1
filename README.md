# Activité Pratique N°1 – Mise en œuvre de PyTorch

## 📌 Présentation

Ce projet a été réalisé dans le cadre de l’**Activité Pratique N°1** et porte sur la découverte et la mise en œuvre du framework **PyTorch**.

L’objectif est de se familiariser progressivement avec PyTorch, depuis la manipulation des tenseurs jusqu’à la création, l’entraînement et l’évaluation de modèles de **Machine Learning** et de **Deep Learning**.

Le projet est organisé en **deux parties** :

- **Partie 1 :** Découverte et bases de PyTorch
- **Partie 2 :** Mise en œuvre de modèles de Machine Learning et Deep Learning avec PyTorch

---

# 🟦 Partie 1 — Découverte et bases de PyTorch

## 🎯 Objectifs

- Installer et configurer l’environnement PyTorch
- Découvrir le framework PyTorch
- Comprendre la notion de tenseur (`Tensor`)
- Créer et manipuler des tenseurs
- Effectuer des opérations sur les tenseurs
- Utiliser PyTorch avec Python
- Comprendre les bases nécessaires à la création de modèles de Deep Learning

## 🧠 Contenu

### 🔹 1. Installation et configuration

- Installation de Python
- Création d’un environnement virtuel
- Installation de PyTorch
- Configuration de l’environnement de travail
- Utilisation de Visual Studio Code et Jupyter Notebook

### 🔹 2. Découverte des tenseurs

- Création de tenseurs
- Dimensions et formes des tenseurs
- Types de données
- Accès aux éléments d’un tenseur
- Modification des tenseurs

### 🔹 3. Opérations sur les tenseurs

- Addition et soustraction
- Multiplication
- Opérations mathématiques
- Changement de dimensions
- Manipulation des dimensions
- Conversion des types de données

### 🔹 4. Premières notions de Deep Learning

- Utilisation des tenseurs comme données d’entrée
- Préparation des données
- Notion de modèle
- Notion de fonction de perte
- Notion d’optimisation

---

# 🟩 Partie 2 — Machine Learning et Deep Learning avec PyTorch

## 🎯 Objectifs

Cette deuxième partie consiste à mettre en pratique les notions étudiées précédemment à travers différents problèmes de **régression**, de **classification** et de **vision par ordinateur**.

Elle contient quatre exercices.

---

## 🔹 Exercice 1 — Régression : prédiction du salaire

### 🎯 Objectif

Prédire le salaire d’une personne à partir de :

- son ancienneté ;
- son degré d’expertise.

### 🛠️ Techniques utilisées

- Création d’un jeu de données synthétique
- Séparation des données en entraînement et test
- Normalisation des variables
- Réseau de neurones avec `nn.Linear`
- Fonction de perte `MSELoss`
- Optimisation avec `SGD`
- Évaluation avec la **MAE (Mean Absolute Error)**

### 🧠 Architecture

```text
Ancienneté + Expertise
          ↓
     Linear(2 → 1)
          ↓
       Salaire
```

---

## 🔹 Exercice 2 — Classification : Iris Dataset

### 🎯 Objectif

Classifier les fleurs Iris en trois espèces :

- Setosa
- Versicolor
- Virginica

### 🛠️ Techniques utilisées

- Dataset Iris de Scikit-learn
- Séparation entraînement/test
- Standardisation avec `StandardScaler`
- Réseau de neurones multicouche
- Fonction d’activation `ReLU`
- Fonction de perte `CrossEntropyLoss`
- Optimiseur `Adam`
- Accuracy
- Matrice de confusion

### 🧠 Architecture

```text
4 caractéristiques
       ↓
Linear(4 → 16)
       ↓
     ReLU
       ↓
Linear(16 → 3)
       ↓
  3 classes
```

---

## 🔹 Exercice 3 — MLP MNIST

### 🎯 Objectif

Reconnaître automatiquement les chiffres manuscrits du dataset **MNIST**.

Le modèle utilisé est un **Multi-Layer Perceptron (MLP)**.

### 🧠 Architecture

```text
Image 28 × 28
      ↓
    Flatten
      ↓
Linear(784 → 128)
      ↓
     ReLU
      ↓
Linear(128 → 10)
      ↓
  10 classes
```

### 🛠️ Éléments étudiés

- `DataLoader`
- Entraînement par mini-batch
- `CrossEntropyLoss`
- Optimiseur `Adam`
- Accuracy
- Precision
- Recall
- F1-score
- Matrice de confusion
- Analyse des images mal classées
- Sauvegarde et chargement du modèle

---

## 🔹 Exercice 4 — CNN MNIST

### 🎯 Objectif

Améliorer la classification des chiffres MNIST grâce à un **réseau de neurones convolutif (CNN)**.

### 🧠 Architecture

```text
Image MNIST
     ↓
   Conv2D
     ↓
    ReLU
     ↓
  MaxPool
     ↓
   Conv2D
     ↓
    ReLU
     ↓
  MaxPool
     ↓
   Flatten
     ↓
   Linear
     ↓
    ReLU
     ↓
  Dropout
     ↓
Linear(128 → 10)
     ↓
 Classification
```

### 🛠️ Techniques utilisées

- `Conv2d`
- `ReLU`
- `MaxPool2d`
- `Flatten`
- Couches linéaires
- `Dropout`
- `CrossEntropyLoss`
- Optimiseur `Adam`
- Évaluation des performances
- Visualisation des erreurs
- Sauvegarde du modèle avec `state_dict`

---

# 🛠️ Technologies utilisées

- **Python 3.11**
- **PyTorch**
- **Torchvision**
- **Scikit-learn**
- **NumPy**
- **Matplotlib**
- **Visual Studio Code**
- **Jupyter Notebook**
- **Git**
- **GitHub**

---

# ⚙️ Installation

## 1. Cloner le dépôt

```bash
git clone https://github.com/khalid-jpg/-Activit-Pratique-N-1.git
```

## 2. Accéder au projet

```bash
cd -Activit-Pratique-N-1
```

## 3. Créer l’environnement virtuel

```bash
python -m venv .venv
```

## 4. Activer l’environnement virtuel sous Windows

```powershell
.venv\Scripts\Activate.ps1
```

## 5. Installer les bibliothèques nécessaires

```bash
pip install torch torchvision torchaudio scikit-learn matplotlib numpy
```

---

# ▶️ Exécution

Le projet peut être exécuté avec **Visual Studio Code** ou **Jupyter Notebook**.

## Avec Visual Studio Code

1. Ouvrir le dossier du projet dans Visual Studio Code.
2. Sélectionner l’environnement Python `.venv`.
3. Ouvrir le notebook correspondant.
4. Exécuter les cellules étape par étape.

## Avec Jupyter Notebook

Lancer :

```bash
jupyter notebook
```

Puis ouvrir le notebook correspondant à la partie ou à l’exercice souhaité.

---

# 📂 Structure du projet

```text
-Activit-Pratique-N-1/
│
├── Partie_1/
│   └── notebooks de la Partie 1
│
├── Exercice_1_Regression_Salaire_PyTorch.ipynb
├── Exercice_2_Iris_PyTorch_Partie_2.ipynb
├── Exercice_3_MNIST_PyTorch_Partie_2.ipynb
├── Exercice_4_CNN_MNIST_PyTorch_Partie_2.ipynb
│
├── README.md
└── .gitignore
```

> **Remarque :** le dossier `.venv/` est un environnement virtuel local et ne doit pas être envoyé sur GitHub.

---

# 📊 Évaluation des modèles

Dans la Partie 2, plusieurs métriques et méthodes d’évaluation sont utilisées :

- **MAE (Mean Absolute Error)** pour la régression
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **Matrice de confusion**
- Visualisation des erreurs de classification

---

# 🎓 Compétences acquises

À travers les deux parties de cette activité, les compétences suivantes ont été développées :

- Configuration d’un environnement Python
- Installation et utilisation de PyTorch
- Manipulation des tenseurs
- Réalisation d’opérations sur les tenseurs
- Préparation et normalisation des données
- Construction de réseaux de neurones
- Entraînement des modèles
- Utilisation des fonctions de perte
- Utilisation des optimiseurs
- Évaluation des modèles
- Classification multi-classes
- Régression
- Utilisation des réseaux MLP
- Utilisation des réseaux CNN
- Visualisation des résultats
- Sauvegarde et chargement des modèles
- Gestion d’un projet avec Git et GitHub

---

# 👨‍💻 Auteur

**Khalid Naitali**

Projet réalisé dans le cadre de l’**Activité Pratique N°1 – Mise en œuvre du Framework PyTorch**.
