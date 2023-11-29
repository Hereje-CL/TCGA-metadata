# TCGA metadata
<p align="justify">
  In cancer research and bioinformatics, correlating The Cancer Genome Atlas (TCGA) IDs with metadata is crucial for extracting meaningful insights from genomic data. TCGA provides a vast repository of genomic information, including gene expression, mutation data, and clinical information from various cancer types. Each sample in TCGA is assigned multiple IDs, which serve as key identifiers. However, the raw data alone may not provide a comprehensive understanding of the underlying biological and clinical characteristics. This is where metadata comes into play.

TCGA metadata includes essential clinical information such as patient demographics, tumor stage, treatment history, and survival outcomes. Correlating TCGA IDs with the metadata allows researchers to link the biological data with relevant clinical details.


When working with TCGA datasets, in most cases we have to spend time to find all identifiers related to the same sample or sequence. 
Unfortunately, this task is not easy, because the metadata documents that can be downloaded from the GDC portal are not complete, and do not correlate the identifiers from one table to the other. 
When downloading the count matrices, each file comes with a unique sequence identifier, but these identifiers are not the same as those found in the metadata acquired directly through the GDC portal. 
This inconsistency in identifiers makes it difficult to assign labels such as vital status, sequencing center or cancer stage to the count matrices for data processing and analyses.

For this reason, we decided to generate filtered metadata tables for each of TCGA's 33 cancer types, based on the [recount package](https://github.com/leekgroup/recount), which uses [GDC and CGC metadata](https://rdrr.io/bioc/recount/man/all_metadata.html) obtained from JSON and XML files. The combined metadata had nested layers that were unnested and multiple empty columns that were deleted. Then, the metadata was organized and divided according to the type of cancer shown in the TCGA code table shown linked below. You can also download [all_metadata_TCGA.tar.xz](https://github.com/Hereje-CL/TCGA-metadata/blob/main/metadata/all_metadata_TCGA.tar.xz) which contains a table showing all 33 TCGA studies.
</p>

Links of interest
======
* [TCGA code table:](https://gdc.cancer.gov/resources-tcga-users/tcga-code-tables/tcga-study-abbreviations) Abbreviations that are found throughout TCGA-related data and documentation.

* [Metadata description:](https://docs.cancergenomicscloud.org/docs/tcga-metadata) Consists of properties, which describe each dataset’s entities, and their values.
