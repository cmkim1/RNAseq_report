# _Eubacterium callanderi_ KIST612

## 1. Bacterial strains and conditions
+ _E. callanderi_ KIST612 cultured in medium with **CO** or **lactate** or **CO&lactate** (triplicates).

## 2. Library preparation & Sequencing
+ RNA QC: Quantity and Quality of RNA were verified with Qubit fluorometer and Nanodrop.
+ Library prep: Zymo-Seq RiboFree® Total RNA Library Kit (Zymo Research).
+ Sequencing: Illumina MiSeq, Reagent V3 (300 PE)
+ Actual yield: 12.4Gbp
+ % PF: 90.34
+ % >= Q30: 79.84
    
Species | Condition | Total reads | Total bases (Mbp)
--- | --- | --- | ---
_E. callanderi_ KIST612 | Lac & CO | 1,397,729 | 839
_E. callanderi_ KIST612 | Lac & CO | 1,806,013 | 1,084
_E. callanderi_ KIST612 | Lac & CO | 1,784,025 | 1,070
_E. callanderi_ KIST612 | CO | 1,614,377 | 969
_E. callanderi_ KIST612 | CO | 1,333,581 | 800
_E. callanderi_ KIST612 | CO | 1,404,991 | 843
_E. callanderi_ KIST612 | Lac | 1,464,498 | 879
_E. callanderi_ KIST612 | Lac | 1,763,046 | 1,058
_E. callanderi_ KIST612 | Lac | 1,957,708 | 1,175
_E. callanderi_ KIST612 | Glc | 1,589,969 | 954
_E. callanderi_ KIST612 | Glc | 1,516,946 | 910
_E. callanderi_ KIST612 | Glc | 1,795,927 | 1,078



## 3. Adapter trimming, alignment, DEG analysis  
All processes were conducted in Galaxy server.  
+ Adapter trimming: Trim Galore! (Galaxy Version 0.6.7+galaxy0)
+ Alignment: BWA-MEM2 (Galaxy Version 2.2.1+galaxy4)
+ Count: featureCounts (Galaxy Version 2.0.3+galaxy2)
+ DEG analysis: edgeR (Galaxy Version 3.36.0+galaxy5)


## 4. DEGs  
Genes without more than 1 CPM in at least 6 samples are insignificant and filtered out.  
638 of 4579 (13.93%) genes were filtered out for low expression.  
TMM was the method used to normalise library sizes.  
  
### 4.1. MDS
MDS visualization of CPM  
All statistical analysis were conducted in R.  

<img src = "https://github.com/user-attachments/assets/f5b4a164-8188-453c-83b7-69b48cb0a1ef" width = "42%" height = "49%">

### 4.2. DEG table (Mix-CO)  
Top 10 up & down regulated genes in Mix compared to CO (FDR < 0.05).
Locus tag | logFC | FDR | Product | KEGG No.
--- | --- | --- | --- | ---
ELI_0615 | 9.4 | 1.91E-06 | hypothetical protein | NA
ELI_2466 | 8.2 | 6.90E-06 | hypothetical protein | NA
ELI_2462 | 8 | 1.92E-06 | hypothetical protein | NA
ELI_0879 | 8 | 4.63E-06 | hypothetical protein | K03310
ELI_2465 | 7.7 | 1.67E-06 | hypothetical protein | K02783
ELI_0616 | 7.6 | 2.72E-06 | Cna B domain protein | NA
ELI_2464 | 7.6 | 1.72E-06 | hypothetical protein | K02782
ELI_0894 | 7.6 | 4.09E-06 | trimethylamine methyltransferase | NA
ELI_2463 | 7.5 | 6.40E-06 | hypothetical protein | K02781
ELI_0600 | 7.4 | 2.00E-06 | hypothetical protein | NA
ELI_3123 | -5 | 0.001 | hypothetical protein | NA
ELI_3134 | -4.8 | 0.006 | hypothetical protein | NA
ELI_3129 | -4.5 | 0.010 | hypothetical protein | NA
ELI_3122 | -4.4 | 0.002 | hypothetical protein | NA
ELI_0570 | -4.4 | 3.42E-04 | hypothetical protein | NA
ELI_3121 | -4.2 | 0.002 | hypothetical protein | NA
ELI_3120 | -4.1 | 0.002 | hypothetical protein | NA
ELI_3293 | -4.1 | 1.89E-04 | transglycosylase associated protein | NA
ELI_3294 | -4 | 0.001 | hypothetical protein | NA
ELI_3130 | -4 | 0.002 | Phage-related protein | K00558
  


### 4.3. KEGG Pathway Enrichment (Mix-CO)  
All statistical analysis and visualizations were conducted in R.  
+ KEGG pathway enrichment analysis
<img src = "https://github.com/user-attachments/assets/34c626d7-01f4-49ce-ae5c-1a43cd34477e" width = "70%" height = "60%">
  

Pathways involved with CO fixation and butyrate synthesis are shown.  
Pathways were colored in [KEGG webpage](https://www.kegg.jp).  

+ Other carbon metabolism (including Wood Ljungdahl pathway)  
<img src = "https://github.com/user-attachments/assets/906d8ef0-077b-41c8-b995-b2c98edace81" width = "100%" height = "80%">
  
+ Butanoate metabolism (including butyrate synthesis)  
<img src = "https://github.com/user-attachments/assets/19cc8cc8-1178-4cf1-a2a7-f24a7906e9b2" width = "100%" height = "68%">


