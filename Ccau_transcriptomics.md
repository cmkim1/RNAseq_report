# Transcriptomics of _Cupriavidus cauae_ PHS1 in Oleic acid

## 1. Bacterial strains and conditions
+ _C. cauae_ PHS1 cultured in MSM + 3g/L (NH4)2SO4 medium with 20 g/L of **oleic acid** or **gluconate** (triplicates).

## 2. Library preparation & Sequencing
+ RNA QC: Quantity and Quality of RNA were verified with Qubit fluorometer and Nanodrop.
+ Library prep: Zymo-Seq RiboFree® Total RNA Library Kit (Zymo Research).
+ Sequencing: Illumina MiSeq, Reagent V3 (300 PE)
+ Actual yield: 18.5Gbp
+ % PF: 86.36
+ % >= Q30: 72.56
    
Species | Condition | Total reads | Total bases (Gbp)
--- | --- | --- | ---
_C. cauae_ PHS1 | Oleic acid | 4,292,082 | 2.453
_C. cauae_ PHS1 | Oleic acid | 4,073,051 | 3.145
_C. cauae_ PHS1 | Oleic acid | 5,585,897 | 3.701
_C. cauae_ PHS1 | Gluconate | 4,089,114 | 2.575
_C. cauae_ PHS1 | Gluconate | 5,241,860 | 2.444
_C. cauae_ PHS1 | Gluconate | 6,168,252 | 3.352


## 3. Adapter trimming, alignment, DEG analysis  
All processes were conducted in Galaxy server.  
+ Adapter trimming: Trim Galore! (Galaxy Version 0.6.7+galaxy0)
+ Alignment: Bowtie2 (Galaxy Version 2.5.3+galaxy1)
+ Count: featureCounts (Galaxy Version 2.0.3+galaxy2)
+ DEG analysis: edgeR (Galaxy Version 3.36.0+galaxy4)


## 4.1 DEGs of _C. cauae_ PHS1 in OA and gluconate medium
Genes were sorted by their differential expression as below.  
Genes without more than 1 CPM in at least 6 samples are insignificant and filtered out.  
190 of 4876 (3.9%) genes were filtered out for low expression.  
  
Category | LogFC (Treated/Control) | Count
---- | ---- | ----
Total protein-coding genes | - | 4,876
Upregulated | LogFC > 1 and FDR < 0.05 | 260
Not significant | \|LogFC\| <= 1 or FDR >= 0.05 | 4,008
Downregulated | LogFC < -1 and FDR < 0.05 | 418

### 4.1.1. MDS plot & MD plot
<img src = "https://github.com/user-attachments/files/20748539/mdsplot_Genome.pdf" width = "45%" height = "45%"><img src = "https://github.com/user-attachments/files/20748542/mdplot_Treatment-Control.pdf" width = "45%" height = "45%" align = "right">

### 4.1.2. Top 20 DEG tables
Product | logFC | P value
---- | ---- | ----
acetyl-CoA C-acyltransferase | 5.14 | 1.68E-11
copper resistance protein CopQ | 5.69 | 3.31E-11
enoyl-CoA hydratase | 4.71 | 3.50E-11
3-hydroxyacyl-CoA dehydrogenase/enoyl-CoA hydratase family protein | 5.46 | 4.70E-11
acyl-CoA dehydrogenase C-terminal domain-containing protein | 5.01 | 9.37E-11
acyl-CoA dehydrogenase family protein | 4.00 | 1.33E-10
TetR/AcrR family transcriptional regulator | 3.76 | 1.52E-10
PaaI family thioesterase | 3.79 | 1.63E-10
3-hydroxyisobutyrate dehydrogenase | 4.42 | 3.69E-10
acyl-CoA-binding protein | 3.45 | 3.71E-10
nitronate monooxygenase family protein | 3.51 | 3.74E-10
beta-lactamase family protein | 3.30 | 4.59E-10
enoyl-CoA hydratase/isomerase family protein | 3.88 | 5.72E-10
nuclear transport factor 2 family protein | 4.63 | 7.04E-10
acyl-CoA dehydrogenase | 3.71 | 7.20E-10
DHA2 family efflux MFS transporter permease subunit | 2.72 | 1.00E-09
hypothetical protein | 5.49 | 1.05E-09
MarR family transcriptional regulator | 4.37 | 1.41E-09
alpha/beta hydrolase | 3.53 | 1.44E-09
bifunctional nicotinamidase/pyrazinamidase | 3.83 | 1.71E-09
