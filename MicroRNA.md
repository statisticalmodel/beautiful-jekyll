---
layout: page
title: MicroRNA Analysis
subtitle:  MicroRNA Analysis Primary Tumors & Metastases in Breast Cancer
---
### My Role
Data Scientist 

### Background
Metastasis is the primary reason to mortality for most cancers, causing 90% of all cancer deaths. 
Breast cancer is considered to be an incurable disease, and although surgery in combination with 
general oncological treatment prolongs the survival in metastatic cancer, there are many patients 
who cannot be helped today. The reason is still unknown, why some tumors metastasis whereas others 
do not. A deeper understanding of the metastatic process would be most valuable to improve and 
ndividualize treatment in this patient group.
 
**MicroRNAs** (miRNAs) are small, ~19-22 nucleotides, non-coding single stranded RNA molecules. 
miRNAs are found in both plants and animals, and are thought to regulate diverse biological processes 
such as cell proliferation, apoptosis and cell differentiation. miRNA deregulation is correlated to human 
cancers, with potential roles of tumor suppressors or oncogenes. This subgroup of miRNAs associated with 
cancer, is often referred to as ‘oncomirs’.

### Purpose
To study the differences in miRNA expression for breast cancer between normal tissue, primary tumors and liver metastases, 
and to evaluate the differences between metastatic and non-metastatic primary tumors, with the aim of finding potential 
therapeutic targets and contribute to the understanding of the mechanisms behind metastasis.

### Data
Microdisected epithelial cells from normal tissue, primary tumor and liver metastases from breast cancer patients have been 
analyzed with microRNA arrays. The raw data material consists of 381 miRNAs, for three different tissue types, from 11 individuals.

<img width="841" alt="2021-02-28_22-03-54" src="https://user-images.githubusercontent.com/15735938/109433491-e1207c00-7a10-11eb-9e22-116739447d84.png">


### Model Used: Mixture model for zero heavy data and empirical Bayes
Mixture model for zero heavy data and empirical Bayes is used to analyze the inference of miRNAs 
and cancer. Four types of false discovery rates are being used to prevent type 1 error. 
These are Benjamini Hochberg, Benjamini Yekutieli, Bonferroni and the Bayesian approach local fdr. 


## Findings 
By analyzing the contrast with the corresponding false discovery rates statistically significant miRNA related to cancer, oncomirs where discovered. 
The study show 39 miRNA with significant differences in expression between normal tissue and primary tumors, and 37 between normal tissue and liver 
metastases. Only one miRNA show significant difference between primary tumor and liver metastases. Our findings include indication that the expression 
increases for miRNA15b in cancer condition. A clinical reduction of miRNA15b could in the future be a potential therapeutic target for cancer.
