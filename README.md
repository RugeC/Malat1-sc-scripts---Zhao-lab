**Long non-coding RNA Malat1 is essential for fine-tuning bone homeostasis through orchestrating cellular crosstalk and the β-catenin-OPG/Jagged1 pathway**

Single cell RNAseq datasets for bone (GSM3674239, GSM3674240, GSM3674241, GSM3674242) and bone marrow (GSM3674243, GSM3674244, GSM3674246) were downloaded from GSE128423. 

Seurat package was applied for downstream analysis. Briefly, genes expressed in fewer than 3 cells and cells with less than 500 genes were filtered out. Cells with over 10% mitochondrial reads and exceeding 6,000 nFeature_RNA were excluded. 

After NormalizeData, the top 5000 variable genes were selected based on dispersion method using FindVariableGenes function of Seurat package. Subsequently, data scaling was performed using the ScaleData function. All datasets were integrated based on the identified anchors. The first 30 principal components for both UMAP (Uniform Manifold Approximation and Projection) and the subsequent application of a graph-based clustering approach were used, with resolution at 0.1. The Clustree function was executed to understand how the structure of clusters changes across different resolutions. 

The FindAllMarkers function was utilized with parameters set to prioritizing positive markers expressed in at least 10% of cells within a cluster and exhibiting a log-fold change threshold of 0.25. 

We utilized Seurat's FeaturePlot to visualize gene expression in individual cells. DotPlot was employed to illustrate the percentage of cells in a cluster expressing a specific gene and to visualize the average scaled expression level of each gene. The distribution of normalized gene expression levels across all cells in each cluster was visualized using VlnPlot function in Seurat. 

R version 4.3.2 and Seurat 5.0.1 were used in the study.
