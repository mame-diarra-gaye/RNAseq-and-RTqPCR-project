# RNAseq-and-RTqPCR-project

Script R et visualisations du projet combiné RNA-Seq et RT-qPCR mené en Licence 3.

Ce dépôt présente un projet académique réalisé dans le cadre d’un TD sur l’analyse de données transcriptomiques et l’interprétation de profils d’expression génique à l’aide du langage R.

##  Objectif

Explorer et comparer les profils d’expression génique à partir de données RT-qPCR et RNA-Seq, à différents stades cellulaires ou types de tissus. L’objectif est d’utiliser des approches statistiques et graphiques pour extraire des informations biologiques pertinentes.

##  Outils utilisés

- DESeq2 : analyse différentielle des gènes à partir des données RNA-Seq
- ggplot2, ggpubr : visualisations graphiques
- tidyverse : manipulation de données
- ComplexHeatmap : visualisation de matrices d’expression
- clusterProfiler, org.Mm.eg.db : enrichissement fonctionnel (Gene Ontology)
- goseq : analyse d’enrichissement GO complémentaire

##  Ce que j’ai appris

- Lire, nettoyer et formater des jeux de données transcriptomiques (RT-qPCR et RNA-Seq)
- Réaliser des visualisations adaptées (boxplots, ACP, heatmaps, MA plot, GO enrichment…)
- Utiliser `DESeq2` pour l’analyse différentielle
- Identifier des gènes significativement exprimés
- Réaliser des analyses d’enrichissement fonctionnel avec `clusterProfiler`
- Interpréter des résultats biologiques à partir de données statistiques
- Organiser un projet reproductible avec RMarkdown et GitHub


Ce projet a été réalisé à des fins d’apprentissage dans le cadre d’un enseignement universitaire. 



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

---

##  Conclusion

Ce projet m’a permis de développer des compétences pratiques en analyse transcriptomique avec R. L’approche combinée RNA-Seq et RT-qPCR m’a aidé à mieux comprendre la complémentarité entre technologies haut-débit et validation ciblée. Ce travail illustre les étapes clés d’un pipeline d’analyse omique reproductible.

