# 🧬 RNAseq-and-RTqPCR-project

Scripts R et visualisations issues d’un projet académique combinant RNA-Seq et RT-qPCR, réalisé en Licence 3 dans le cadre d’un TD sur l’analyse de données transcriptomiques.

---

##  Objectif du projet

Explorer et comparer les profils d’expression génique à partir de données RT-qPCR et RNA-Seq, à différents stades cellulaires ou types de tissus.  
L’objectif : mobiliser des outils statistiques et graphiques sous R pour identifier des régulations d’intérêt biologique.

---

## 🧰 Outils et packages utilisés

- **DESeq2** : analyse différentielle des gènes (RNA-Seq)
- **ggplot2**, **ggpubr** : visualisations graphiques
- **tidyverse**, **dplyr**, **tidyr** : manipulation et nettoyage de données  
- **ComplexHeatmap** : représentation de matrices d’expression
- **clusterProfiler**, **org.Mm.eg.db** : enrichissement fonctionnel (GO)
- **goseq** : analyse GO complémentaire

---

##  Ce que ce projet m’a appris

- Lire, nettoyer et formater des données transcriptomiques (RT-qPCR et RNA-Seq)
- Réaliser des visualisations claires (boxplots, ACP, heatmaps, MA plot, GO enrichment…)
- Identifier des gènes différentiellement exprimés à l’aide de `DESeq2`
- Explorer des voies biologiques via des analyses d’enrichissement GO
- Structurer un pipeline d’analyse reproductible avec **RMarkdown** et **GitHub**

> Ce projet a été mené dans un cadre pédagogique, avec pour objectif de se former à l’analyse de données omiques.

---

## 📊 Visualisations

### 🟦 RT-qPCR – Boîte à moustaches des valeurs MedCt

Comparaison de la distribution des valeurs de MedCt par échantillon.

![Boxplot MedCt](boxplot_medct_gdm.png)


###  Analyse en composantes principales (ACP)

#### PC1 vs PC2 selon les échantillons  
Séparation visible entre certains groupes, indiquant des profils d’expression distincts.  
![PC1-PC2 échantillons](PCA_PC1_PC2_par_echantillon.png)

#### PC1 vs PC2 selon les réplicats biologiques  
Les réplicats se superposent bien → bonne reproductibilité.  
![PC1-PC2 bioRep](PCA_PC1_PC2_par_bioRep.png)

#### PC1 vs PC3 selon les échantillons  
Visualisation complémentaire du 3e axe de variation.  
![PC1-PC3 échantillons](PCA_PC1_PC3_par_echantillon.png)

---

## 🧬 RNA-Seq – Analyses différentielles & enrichissement

### PCA plot selon le type de tissu  
![PCA RNAseq](PCA_Plot_source_name.png)

### MA plot (résultats DESeq2)  
![MA plot DESeq2](MA_plot_res.png)

### MA plot amélioré (`ggmaplot`)  
![ggmaplot DEGs](MA_plot_ggmaplot_DEGs_Liver_vs_Cerebellum.png)

### Heatmap des 30 gènes les plus différenciés  
![Heatmap top30 DEGs](heatmap_top30_DEGs.png)

### Heatmap de 100 gènes sélectionnés  
![Heatmap top100 genes](heatmap_top100_genes.png)

### Dotplot – Enrichissement GO (Biological Process)  
![GO enrichment dotplot](GO_Enrichment_dotplot.png)

---

## Conclusion

Ce projet m’a permis de développer des compétences concrètes en analyse de données transcriptomiques.  
L’approche combinée RNA-Seq / RT-qPCR m’a aidée à mieux comprendre la complémentarité entre technologies haut-débit et validation ciblée.  
Je retiens aussi l’importance de la reproductibilité, de la clarté des visualisations et de l’interprétation biologique des résultats.

