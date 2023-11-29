# TCGA-metadata
Filtered TCGA metadata with all the necessary IDs for downstream analyses

When working with TCGA datasets, in most cases we have to spend time to find all identifiers related to the same sample or sequence. 
Unfortunately, this task is not easy, because the metadata documents that can be downloaded from the GDC portal are not complete, and do not correlate the identifiers from one table to the other. 
When downloading the count matrices, each file comes with a unique sequence identifier, but these identifiers are not the same as those found in the metadata files under the names "Case ID" or "File ID". 
This inconsistency in identifiers makes it difficult to assign labels such as vital status, sequencing center or cancer stage to the count matrices for machine learning predictors.

Because of this, I decided to generate filtered metadata tables for each of TCGA's 33 cancer types, based on the [recount package](https://github.com/leekgroup/recount), which uses [GDC and CGC metadata](https://rdrr.io/bioc/recount/man/all_metadata.html) obtained from JSON and XML files. The combined metadata has nested layers that were unnested and multiple empty columns that were deleted. Then, the metadata was organized according to the type of cancer shown in the table below. You can also download [all_metadata_TCGA.tar.xz](https://github.com/Hereje-CL/TCGA-metadata/blob/main/all_metadata_TCGA.tar.xz) which consists of a table showing all 33 TCGA studies.


TCGA code table
======
Abbreviation | Study Name
:---: | :---:
`ACC` |	Adrenocortical carcinoma
`BLCA` | Bladder Urothelial Carcinoma
`BRCA` | Breast invasive carcinoma
`CESC` |	Cervical squamous cell carcinoma and endocervical adenocarcinoma
`CHOL` |	Cholangiocarcinoma
`COAD` |	Colon adenocarcinoma
`DLBC` |	Lymphoid Neoplasm Diffuse Large B-cell Lymphoma
`ESCA` |	Esophageal carcinoma
`GBM` |	Glioblastoma multiforme
`HNSC` |	Head and Neck squamous cell carcinoma
`KICH` |	Kidney Chromophobe
`KIRC` |	Kidney renal clear cell carcinoma
`KIRP` |	Kidney renal papillary cell carcinoma
`LAML` |	Acute Myeloid Leukemia
`LGG` |	Brain Lower Grade Glioma
`LIHC` |	Liver hepatocellular carcinoma
`LUAD` |	Lung adenocarcinoma
`LUSC` |	Lung squamous cell carcinoma
`MESO` |	Mesothelioma
`OV` |	Ovarian serous cystadenocarcinoma
`PAAD` |	Pancreatic adenocarcinoma
`PCPG` |	Pheochromocytoma and Paraganglioma
`PRAD` |	Prostate adenocarcinoma
`READ` |	Rectum adenocarcinoma
`SARC` |	Sarcoma
`SKCM` |	Skin Cutaneous Melanoma
`STAD` |	Stomach adenocarcinoma
`TGCT` |	Testicular Germ Cell Tumors
`THCA` |	Thyroid carcinoma
`THYM` |	Thymoma
`UCEC` |	Uterine Corpus Endometrial Carcinoma
`UCS` |	Uterine Carcinosarcoma
`UVM` |	Uveal Melanoma
