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

##  Analyse RNA-Seq

L’analyse RNA-Seq a été réalisée pour détecter les gènes différentiellement exprimés entre différents tissus (foie, rein, cervelet) à l’aide du package **DESeq2**. Plusieurs visualisations ont été produites pour interpréter les résultats.

---

###  PCA sur les échantillons RNA-Seq

Une analyse en composantes principales (ACP) a été effectuée après transformation par variance stabilisée (`vst`) pour explorer la variance globale des données.

![PCA RNAseq](PCA_Plot_source_name.png)

---

###  Plot MA

Le graphique MA permet de visualiser les gènes exprimés différemment en fonction de leur niveau d'expression moyen.

![MA Plot](MA_plot_deseq2.png)

---

###  Volcano Plot (ggmaplot)

Le `ggmaplot` met en évidence les gènes significativement sur- ou sous-exprimés. Les gènes les plus différenciés sont annotés.

![ggmaplot](ggmaplot_deseq2.png)

---

###  Heatmap des 30 gènes les plus variables

Une carte de chaleur a été générée à partir des 30 gènes les plus variables parmi ceux significativement exprimés.

![Heatmap top30](heatmap_top30.png)

---

###  Heatmap des 100 premiers gènes exprimés

Une deuxième carte de chaleur montre l’expression des 100 gènes les plus fortement exprimés, permettant d'observer les regroupements entre échantillons.

![Heatmap 100 gènes](heatmap_top100.png)

---

###  Enrichissement fonctionnel (GO)

L’enrichissement en ontologies biologiques (GO) a été réalisé avec `clusterProfiler`. Les processus biologiques surreprésentés chez les gènes différentiellement exprimés ont été identifiés.

![GO dotplot](GO_Enrichment_dotplot.png)


