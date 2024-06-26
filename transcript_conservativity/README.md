## ✨ Transcript Conservation Assessment

### Overview
This repository contains scripts and notebooks for the analysis of transcript conservation in human genes. 
The analysis combines information about genetic variations in transcripts with expression data and
classic conservativity metrics to gain insights into transcript conservation across genes.
#### Code Directory

[vcf_parser.py](code/vcf_parser.py) - Script for parsing VCF files to collect necessary data.

> Usage:
> ```python
> from vcf_parser import vcf_parsing
> vcf_parsing('../data/NAME_OF_YOUR_FILE.vcf')
> ```

[data_processing_functions.py](code/data_processing_functions.py) - Script for collecting information about transcripts

> Usage:
> ```python
> from data_processing_functions import info_collecting, info_filtering
> all_gene_dataframe = info_collecting(files_names)
> final_transcipt_data = info_filtering(all_gene_dataframe, constraint_file, expression_file)
> ```

[gnomad_vcf_parser.ipynb](code/gnomad_vcf_parser.ipynb) - Jupyter notebook demonstrating the usage of `vcf_parsing` from vcf_parser.py.

[all_chr_genvar_analysis.ipynb](code/all_chr_genvar_analysis.ipynb) - Jupyter notebook illustrating gene analysis from all chromosomes,
focusing on chromosome 13.
The analysis integrates information on transcript variants, expression levels obtained from GTEx portal, and
conservativity metrics from gnomAD database.

[all_genes_analysis.ipynb](code/all_genes_analysis.ipynb) - Jupyter notebook providing insights into all human genes
and outlining the gene selection process for further investigation.

[expression_data_collecting.ipynb](code/expression_data_collecting.ipynb) - Script for collecting transcript expression data from GTEx Transcript TPMs data.

[gene_examples_analysis.ipynb](code/gene_examples_analysis.ipynb) - Analysis of transcript examples from selected genes for subsequent phases of the study.

#### Data directory

[example_chr22.vcf](data/example_chr22.vcf) - VCF file containing genetic variation data for chromosome 22.

[max_tissue_median_expr.tsv](data/max_tissue_median_expr.tsv) - TSV file with maximum median tissue expression data.

[all_genes_analysis.tsv](data/all_genes_analysis.tsv) - TSV file with detailed analysis of all human genes.

[example_genes_transcripts.tsv](data/example_genes_transcripts.tsv) - TSV file with transcripts of example genes data.

[Plots directory](data/plots) contains plots generated from the Jupyter notebooks included in the repository.

For additional details, refer to the specific files and directories within this repository.
