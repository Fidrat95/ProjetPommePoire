# 🍎 Projet Pomme-Poire 🍐 | Reconnaissance de formes par IA

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white)

[cite_start]**Projet académique - ECE (École d'Ingénieurs) - Cycle ING3** [cite: 1, 3]  
[cite_start]**Méthodologie :** Cycle en V [cite: 16, 181]

## 📝 Description du Projet
[cite_start]Ce projet consiste à concevoir un système embarqué intelligent capable de distinguer une pomme d'une poire à partir d'une photographie[cite: 11]. [cite_start]Le système repose sur un Réseau de Neurones Convolutif (CNN) entraîné sur ordinateur (Google Colab) et déployé sur un microcontrôleur ESP32[cite: 13, 15, 92]. 

## ⚙️ Fonctionnalités (Exigences)
[cite_start]Le projet répond à 6 fonctions secondaires (FS)[cite: 40, 41, 42, 43]:
- [cite_start]**FS1 :** Capture d'une image via une caméra miniature et affichage sur un écran TFT[cite: 40].
- **FS2 :** Inférence locale sur l'ESP32. [cite_start]Allumage d'une **diode verte** pour une pomme, ou **rouge** pour une poire[cite: 40, 96].
- [cite_start]**FS3 :** Calcul et affichage du pourcentage de confiance de la prédiction[cite: 41].
- [cite_start]**FS4 :** Transfert de la photographie prise par l'ESP32 vers un ordinateur via communication série (CoolTerm)[cite: 41, 74].
- [cite_start]**FS5 :** Vérification de l'image sur l'ordinateur via un script Python avec affichage de la confiance[cite: 42].
- [cite_start]**FS6 :** Extraction et affichage des images intermédiaires (*Feature Maps*) générées par les couches de convolution du CNN[cite: 43].

## 🛠️ Matériel Requis
- [cite_start]Carte microcontrôleur **ESP32**[cite: 13].
- [cite_start]Caméra couleur miniature **OV2640**[cite: 14].
- [cite_start]Écran couleur **TFT 2.0**[cite: 14].
- [cite_start]Diodes LED (Rouge et Verte)[cite: 24].
- [cite_start]Kit d'électronique de base (câbles, breadboard)[cite: 13].

## 📂 Architecture du Dépôt

\`\`\`text
📦 ProjetPommePoire
 ┣ 📂 dataset/      # (Ignoré par Git) Dossiers d'images : train/, validation/, test/
 ┣ 📂 docs/         # Rapport final de projet (format LaTeX et PDF)
 ┣ 📂 firmware/     # Scripts C++ / Arduino pour l'ESP32 (Contrôle Caméra, Écran, Inférence)
 ┣ 📂 notebooks/    # Notebooks Google Colab/Jupyter (.ipynb) pour l'entraînement du CNN
 ┗ 📜 README.md     # Documentation du projet
\`\`\`

## 🚀 Démarrage Rapide

### 1. Entraînement du Modèle (Python)
1. Ouvrir le script situé dans `notebooks/` via Google Colab ou Jupyter Notebook.
2. Assurez-vous d'avoir le dataset structuré en dossiers `apple` et `pear`.
3. Le script intègre la normalisation des images (96x96 pixels) et la *Data Augmentation*.
4. Le modèle entraîné est exporté au format `.keras` ou `.tflite` (pour l'embarqué).

### 2. Déploiement Embarqué (C++)
1. Ouvrir le dossier `firmware/` avec l'IDE Arduino ou PlatformIO.
2. [cite_start]Importer les bibliothèques requises pour l'écran TFT et la caméra OV2640[cite: 54].
3. Flasher le code sur l'ESP32.

## 👥 Auteurs
- **Aurel** - *Développement CNN & Hardware* - **Fidrat95** - *Développement CNN & Hardware* - [Profil GitHub](https://github.com/Fidrat95)