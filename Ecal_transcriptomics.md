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


## 4.1 DEGs 
  

### 4.1.1. MDS
MDS visualization of CPM  
All statistical analysis were conducted in R.  

<img src = "https://github.com/user-attachments/files/22257877/DimentionReductionPlots.pdf" width = "55%" height = "55%">

### 4.1.2. DEG table

### 4.2. KEGG Pathway Enrichment  
