# Projets de Modélisation Stochastique et Machine Learning

Ce dépôt regroupe 3 travaux pratiques réalisés par Sara EL Bari et Auriane Delcroix sous forme de Jupyter Notebooks, couvrant les exercices demandés.

## 📋 Sommaire

1. [Approximation Gaussienne d'une loi de Poisson](#1-approximation-gaussienne-dune-loi-de-poisson)
2. [Algorithme PageRank et Marches Aléatoires](#2-algorithme-pagerank)
3. [Régression par Processus Gaussiens (Airfoil Self-Noise)](#3-régression-par-processus-gaussiens)

---

## 1. Approximation Gaussienne d'une loi de Poisson
**Fichier :** `exercice_1.ipynb`

Ce projet étudie la convergence en loi de la variable de Poisson centrée-réduite vers une loi normale standard $\mathcal{N}(0,1)$.

* **Objectif :** Analyser la distance de Kolmogorov $\alpha_n$ entre une loi $\mathcal{P}(n)$ et sa limite gaussienne.
* **Points clés :**
    * Visualisation de l'écart réel entre les fonctions de répartition.
    * Étude empirique de la vitesse de convergence (en $1/\sqrt{n}$).
    * Comparaison avec les bornes théoriques de Berry-Esseen.
 
## 2. Algorithme PageRank
**Fichier :** `pagerank_project.ipynb`

Étude du fonctionnement de l'algorithme PageRank pour le classement de nœuds dans un réseau.

* **Expérimentations :**
    * **Graphes Aléatoires :** Génération de graphes d'Erdős–Rényi et calcul du score d'importance théorique via la méthode de la puissance itérée.
    * **Simulation :** Estimation de la distribution stationnaire par des marches aléatoires (Monte Carlo) de longueurs croissantes ($10^3$ à $10^7$).
    * **Cas Réel :** Application au réseau de Zachary (club de karaté) pour identifier les membres influents.
* **Analyse :** Comparaison de la précision des classements obtenus par simulation par rapport aux valeurs théoriques.


## 3. Régression par Processus Gaussiens
**Fichier :** `Regression_gaussienne.ipynb`

Application des méthodes de régression non-paramétrique sur le jeu de données *Airfoil Self-Noise* de l'UCI.

* **Problématique :** Prédire le niveau de pression acoustique (bruit) de profils d'ailes de la NASA en fonction de variables physiques (fréquence, angle d'attaque, vitesse, etc.).
* **Méthodologie :**
    * Exploration et normalisation des données.
    * Implémentation de modèles à noyaux (Linéaire vs RBF).
    * Optimisation des hyperparamètres et évaluation des performances (R², Log-vraisemblance).
* **Résultat :** Le modèle à noyau RBF montre une meilleure capacité à capturer les non-linéarités du phénomène physique.

---
## Installation et Prérequis

Pour exécuter ces notebooks, vous aurez besoin de Python 3 et des bibliothèques suivantes :

```bash
pip install numpy pandas matplotlib scipy networkx ucimlrepo
