# Transcriptomics of _E. coli_ K-12 MG1655 (MAGE)

## 1. Bacterial strains and conditions
+ _Escherichia coli_ K-12 MG1655 containing _mut_S::pRED-1 in genome (EcSIM1F) and RBS mutataion upstream of _crp_ and _fis_ (EcSIM1F1).
+ Both strains contain two plasmids pFABT and pBbB6k_tesA.  
3 replicates of EcSIM1F and EcSIM1F1 were cultured in M9 medium.  

## 2. Library preparation & Sequencing
+ RNA QC: RIN of all RNA samples were higher than 7.0. Quantity and Quality of RNA were verified with Qubit fluorometer and Nanodrop.
+ Library prep: Zymo-Seq RiboFree® Total RNA Library Kit (Zymo Research).
+ Sequencing: MiSeq, Reagent V3 (300 PE)
+ Actual yield: 17.37GB
+ % PF: 91.69%
+ % >= Q30: 77.58%
    
Species | Condition | Total reads | Total bases (Gbp)
--- | --- | --- | ---
_E. coli_ SIM1F1 | MAGE | 4,653,795 | 2.619
_E. coli_ SIM1F1 | MAGE | 4,647,314 | 2.616
_E. coli_ SIM1F1 | MAGE | 5,156,824 | 2.903
_E. coli_ SIM1F | Control | 4,904,075 | 2.76
_E. coli_ SIM1F | Control | 4,949,749 | 2.786
_E. coli_ SIM1F | Control | 5,368,837 | 3.022


## 3. Adapter trimming, alignment, DEG analysis  
All processes were conducted in Galaxy server.  
+ Adapter trimming: Trim Galore! (Galaxy Version 0.6.7+galaxy0)
+ Alignment Bowtie2 (Galaxy Version 2.5.3+galaxy1)
+ Count: featureCounts (Galaxy Version 2.0.3+galaxy2)
+ DEG analysis: edgeR (Galaxy Version 3.36.0+galaxy4)


## 4.1 _E. coli_ SIM1F1 - pFABT and pBbB6k_tesA
Genes were sorted by their differential expression as below.  
Genes without more than 1 CPM in at least 6 samples are insignificant and filtered out.  
303 of 4325 (7.01%) genes were filtered out for low expression.  
  
Category | LogFC (Treated/Control) | Count
---- | ---- | ----
Total protein-coding genes | - | 4,325
Upregulated | LogFC > 1 and FDR < 0.05 | 125
Not significant | \|LogFC\| <= 1 or FDR >= 0.05 | 3584
Downregulated | LogFC < -1 and FDR < 0.05 | 313

### 4.1.1. MDS plot & MD plot
<img src = "https://github.com/user-attachments/files/20084271/mdsplot_Genome.pdf" width = "45%" height = "45%"><img src = "https://github.com/user-attachments/files/20084278/mdplot_MAGE-Control.pdf" width = "45%" height = "45%" align = "right">

### 4.1.2. Top 20 DEG tables
Product | logFC | P value
---- | ---- | ----
Regulatory protein SoxS | -4.91 | 4.92E-38
Small heat shock protein IbpB | -4.78 | 2.09E-35
Tetracycline resistance protein%2C class C | -4.12 | 9.02E-41
Small heat shock protein IbpA | -3.69 | 8.78E-37
Periplasmic protein CpxP | -3.66 | 1.16E-23
Fumarate hydratase class II | -3.53 | 3.32E-33
hypothetical protein | -3.44 | 1.93E-33
Ferric enterobactin transport system permease protein FepD | -3.28 | 2.26E-18
Outer membrane porin F | -3.05 | 9.36E-33
Magnesium-transporting ATPase%2C P-type 1 | -2.98 | 8.02E-35
Nitrite transporter NirC | 5.51 | 1.5E-32
Nitrite reductase (NADH) small subunit | 4.65 | 1.46E-26
Respiratory nitrate reductase 1 beta chain | 4.54 | 5.16E-36
Nitrate/nitrite transporter NarK | 4.17 | 5.04E-36
Nitrate reductase molybdenum cofactor assembly chaperone NarJ | 4.01 | 2.64E-24
Periplasmic nitrate reductase | 3.93 | 6.09E-29
Respiratory nitrate reductase 1 gamma chain | 3.73 | 1.16E-12
Nitrite reductase [NAD(P)H] | 3.67 | 1.31E-36
Cytochrome c-552 | 3.65 | 2.52E-28
Respiratory nitrate reductase 1 alpha chain | 3.52 | 5.77E-26
