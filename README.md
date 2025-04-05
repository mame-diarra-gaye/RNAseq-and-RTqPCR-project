# RNAseq-and-RTqPCR-project
Script R et visualisations du projet RNA-Seq mené en licence 3

Ce dépôt présente un projet académique réalisé en Licence 3, dans le cadre d’un TD sur l’analyse de données transcriptomiques.

## Objectif

Explorer les profils d’expression génique à partir de données RNA-Seq et RT-qPCR à différents stades cellulaires, en utilisant R et divers packages statistiques.

## Outils utilisés

- DESeq2, tidyverse, dplyr, tidyr, ggplot2, ggpbur
  

## Ce que j’ai appris

- Lire et nettoyer des données transcriptomiques
- Réaliser des visualisations claires (ggplot2)
- Utiliser R pour explorer des jeux de données biologiques

## Avertissement

Ce projet a été réalisé à des fins d’apprentissage dans le cadre universitaire.


##  Visualisations

###  Boîte à moustaches des valeurs MedCt par échantillon

Ce graphique permet de comparer la distribution des valeurs de MedCt pour chaque échantillon. On observe une homogénéité des médianes, ce qui peut indiquer une bonne qualité de mesure.

![Boxplot MedCt](boxplot_medct_gdm.png)


---

###  Analyse en composantes principales (ACP)

L'ACP a été réalisée pour explorer la structure des données transcriptomiques et identifier d’éventuelles séparations entre les échantillons.

#### PC1 vs PC2 selon les échantillons  
On observe une séparation nette entre certains groupes, suggérant des profils d'expression distincts entre échantillons.

![PC1-PC2 échantillons](PCA_PC1_PC2_par_echantillon.png)

#### PC1 vs PC2 selon les réplicats biologiques  
La superposition des réplicats dans l’espace factoriel confirme une bonne reproductibilité des mesures.

![PC1-PC2 bioRep](PCA_PC1_PC2_par_bioRep.png)

#### PC1 vs PC3 selon les échantillons  
Cette projection permet de mieux visualiser la contribution du troisième axe dans la différenciation des groupes.

![PC1-PC3 échantillons](PCA_PC1_PC3_par_echantillon.png)

---

###  Visualisations RNA-Seq

####  PCA plot selon le type de tissu (`source_name`)

Ce graphique montre la séparation nette des échantillons selon leur origine (Cerebellum, Kidney, Liver).

![PCA RNAseq](PCA_Plot_source_name.png)

####  MA plot des résultats DESeq2

Le MA plot montre la distribution des gènes en fonction de l’intensité moyenne et du log2 fold change. Les gènes significativement différenciés sont mis en évidence.

![MA plot DESeq2](MA_plot_res.png)

####  MA plot amélioré avec `ggmaplot`

Cette version plus esthétique permet de mieux visualiser les gènes up/down régulés.

![ggmaplot DEGs](MA_plot_ggmaplot_DEGs_Liver_vs_Cerebellum.png)

####  Heatmap des 30 gènes les plus différenciés

Cette carte de chaleur représente les profils d'expression des 30 gènes les plus régulés entre les groupes.

![Heatmap top30 DEGs](heatmap_top30_DEGs.png)

####  Heatmap des 100 gènes les plus variables

Cette heatmap donne une vue globale de la variabilité des 100 gènes les plus exprimés.

![Heatmap top100 genes](heatmap_top100_genes.png)

####  Enrichissement fonctionnel GO (Biological Process)

Les gènes différentiellement exprimés ont été soumis à une analyse d’enrichissement GO. Les processus biologiques enrichis sont représentés ci-dessous.

![GO enrichment dotplot](GO_Enrichment_dotplot.png)
