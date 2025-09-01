🧬 WGCNA Pipeline for RNA-Seq Adipogenesis Study

#_________This is for demonstration purpose only___________#

#________The official WGCNA website recommends at least 15 samples for analysis____________#


This repository provides an **end-to-end R workflow** for **Weighted Gene Co-expression Network Analysis (WGCNA)** on RNA-Seq data.  
It is built around the public dataset [**GSE223846**](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE223846), focusing on the molecular regulation of **PPARγ-mediated adipogenesis**.

---

## 🚀 Features

- **Data fetching & preprocessing**
  - Import raw gene counts and metadata directly from GEO
  - Harmonize sample metadata with expression matrix
  - Remove low-quality genes and samples

- **Quality control**
  - Outlier detection (hierarchical clustering, PCA)
  - Violin plots of gene counts (before/after normalization)

- **Normalization**
  - Gene filtering with DESeq2
  - Variance stabilizing transformation (VST)

- **Network construction**
  - Soft-threshold power selection
  - Signed TOM-based blockwise module detection
  - Dendrogram visualization with module colors

- **Module–trait relationships**
  - Trait binarization and correlation with module eigengenes
  - Heatmaps of module–trait associations

- **Intramodular analysis**
  - Module membership (kME) and gene significance (GS)
  - Hub gene identification
  - Export of ranked hub genes to Excel

---

## 📊 Outputs

- **QC plots**: PCA, clustering dendrograms, violin plots  
- **Network plots**: Scale-free topology plots, module dendrograms  
- **Heatmaps**: Module–trait correlation matrices  
- **Excel results**: Ranked hub genes by module  

---

## 🛠️ Requirements

The pipeline is written in **R (≥ 4.2)** and requires the following packages:

- [WGCNA](https://cran.r-project.org/package=WGCNA)  
- [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html)  
- [GEOquery](https://bioconductor.org/packages/release/bioc/html/GEOquery.html)  
- tidyverse  
- ComplexHeatmap  
- pheatmap  
- gridExtra  
- writexl

Install missing packages using:
```r
install.packages(c("WGCNA", "tidyverse", "pheatmap", "gridExtra", "writexl"))
BiocManager::install(c("DESeq2", "GEOquery", "ComplexHeatmap"))

🔬 Use Case

This workflow was designed to study the role of PPARγ in adipogenesis using transcriptomic data, but it can be adapted to any RNA-Seq dataset for co-expression network analysis.




install.packages(c("WGCNA", "tidyverse", "pheatmap", "gridExtra", "writexl"))
BiocManager::install(c("DESeq2", "GEOquery", "ComplexHeatma
