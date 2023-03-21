# Microbiome-analysis

The aim of the work is the analysis of the expression of microbes residing in the oral cavity. Taking a group of inhabitants of the Fiji Islands as the analysis population, we want to evaluate whether there are differentially abundant microorganisms between males and females or between different age groups.  

For differential abundance analyzes of microorganisms we use the methods edgeR which fits a negative binomial model and limma-voom which fits a linear model with weights and both edgeR and limma-voom with weights calculated using a negative binomial to zero inflation (zinbFit).  
After evaluating four types of normalization, full-quantile, upper-quartile, RLE and TMM, based on the results obtained, we choose to proceed with the latter for subsequent analyses. The method TMM, in general, seems to perform better on datasets with a high percentage of zeros, which is precisely the case for metagenomics data.

The dataset was obtained from Bioconductor's package "curatedMetagenomicData" which provides the abundance of taxonomic, functional and genetic markers for samples collected from different sites in the human body.
