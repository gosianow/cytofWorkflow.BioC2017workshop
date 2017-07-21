# CyTOF workflow: differential discovery in high-throughput high-dimensional cytometry datasets
# BioC 2017 workshop


## Abstract 

High dimensional mass and flow cytometry (HDCyto) experiments have become a method of choice for high throughput interrogation and characterization of cell populations. Here, we present an R-based pipeline for differential analyses of HDCyto data, largely based on Bioconductor packages. We computationally define cell populations using FlowSOM clustering, and facilitate an optional but reproducible strategy for manual merging of algorithm-generated clusters. Our workflow offers different analysis paths, including association of cell type abundance with a phenotype or changes in signaling markers within specific subpopulations, or differential analyses of aggregated signals. Importantly, the differential analyses we show are based on regression frameworks where the HDCyto data is the response; thus, we are able to model arbitrary experimental designs, such as those with batch effects, paired designs and so on. In particular, we apply generalized linear mixed models to analyses of cell population abundance or cell-population-specific analyses of signaling markers, allowing overdispersion in cell count or aggregated signals across samples to be appropriately modeled. To support the formal statistical analyses, we encourage exploratory data analysis at every step, including quality control (e.g. multi-dimensional scaling  plots), reporting of clustering results (dimensionality reduction, heatmaps with dendrograms) and differential analyses (e.g. plots of aggregated signals).


***Note:*** The full version of this workflow is available at F1000 under the link: https://f1000research.com/articles/6-748/v1 and at Bioconductor workflows under the link: http://bioconductor.org/help/workflows/cytofWorkflow/

## Installation 

First you need to install `BiocInstaller`:

```
source("http://bioconductor.org/biocLite.R")
```

Specify to use bioc-devel (3.6):

```
useDevel()
```

You need to install the `devtools` package for the special use of `biocLite()` below:

```
biocLite("devtools") 
```

Install the workflow from this github repository:

```
biocLite("gosianow/cytofWorkflow.BioC2017workshop", build_vignettes = TRUE, dependencies = TRUE)
```

After the installation you can follow the workflow described in the vignette, which you can access with the following command:

```
browseVignettes("cytofWorkflow.BioC2017workshop")
```





