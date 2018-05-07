# Advanced Practical in Molecular Biology Project
Metagenomic analysis of soil samples using QIIME on Cirrus HPC
## Scripts

1. [validate_mapping_file.py](./scripts/validation.pbs)
This script validates the original mapping file in order to make sure that it is formatted correctly.
1. [split_libraries_fastq.py](./scripts/split_libraries.pbs)
This script demultiplexes sequence data (in Fastq format) and performes quality filtering at Phred >= Q20, because base calls with a Q-score values that are lower than 20 are considered low quality.
1. [pick_closed_reference_otus.py](./scripts/picking_OTUs.pbs)
This script was used for picking operational taxonomical units (OTUs) using closed reference approach, i.e. against the database of known centroids (here Greengenes).
1. [core_diversity_analyses.py](./scripts/core_diversity.pbs)
This workflow script includes several diversity analyses, such as alpha diversity and rerefaction plots, beta diversity and taxa tables.
1. [compare_categories.py](./scripts/statistics_pH.pbs)
This script allows to analyse the statistical significance of sample groupings using distance matrices. ANOSIM method was used. This method allows testing whether two or more groups of samples are significantly different based on a categorical variable from the mapping file (here pH of the soil). The same script was adopted to evaluate the effect of other categories in the mapping file.
