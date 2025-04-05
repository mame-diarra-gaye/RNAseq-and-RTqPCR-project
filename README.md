# RNAseq-and-RTqPCR-project
Script R et visualisations du projet RNA-Seq mené en licence 3

Ce dépôt présente un projet académique réalisé en Licence 3, dans le cadre d’un TD sur l’analyse de données transcriptomiques.

## Objectif

Explorer les profils d’expression génique à partir de données RNA-Seq et RT-qPCR à différents stades cellulaires, en utilisant R et divers packages statistiques.

## Outils utilisés

-  R, tidyverse, dplyr, tidyr, ggplot2
  

## Ce que j’ai appris

- Lire et nettoyer des données transcriptomiques
- Réaliser des visualisations claires (ggplot2)
- Utiliser R pour explorer des jeux de données biologiques

## Avertissement

Ce projet a été réalisé à des fins d’apprentissage dans le cadre universitaire.


##  Visualisations

###  Boîte à moustaches des valeurs MedCt par échantillon

Ce graphique permet de comparer la distribution des valeurs de MedCt pour chaque échantillon. On observe une homogénéité des médianes, ce qui peut indiquer une bonne qualité de mesure.

![Boxplot MedCt](figures/boxplot_MedCt_echantillons.png)

---

###  Analyse en composantes principales (ACP)

L'ACP a été réalisée pour explorer la structure des données transcriptomiques et identifier d’éventuelles séparations entre les échantillons.

#### PC1 vs PC2 selon les échantillons  
On observe une séparation nette entre certains groupes, suggérant des profils d'expression distincts entre échantillons.

![PCA PC1-PC2 echantillon](figures/PCA_PC1_PC2_echantillon.png)

#### PC1 vs PC2 selon les réplicats biologiques  
La superposition des réplicats dans l’espace factoriel confirme une bonne reproductibilité des mesures.

![PCA PC1-PC2 bioRep](figures/PCA_PC1_PC2_bioRep.png)

#### PC1 vs PC3 selon les échantillons  
Cette projection permet de mieux visualiser la contribution du troisième axe dans la différenciation des groupes.

![PCA PC1-PC3 echantillon](figures/PCA_PC1_PC3_echantillon.png)

