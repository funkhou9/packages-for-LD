# packages-for-LD

> A list of existing software (preferably R packages) that include implementation
> to estimate genome-wide levels of linkage disequilibrium

Ideally, correlations between SNPs are measured using the following eqn:

![](http://latex.codecogs.com/gif.latex?r%5E2_%7Bij%7D%20%3D%20%5Cfrac%7B(p_%7Bij%7D%20-%20p_ip_j)%5E2%7D%7Bp_i(1%20-%20p_i)p_j(1%20-%20p_j)%7D)

where p_i is the marginal frequency of allele B at the ith SNP, and p_ij is the joint frequency of allele B at the ith and jth SNP, as they appear together on the same haplotype

[trio (Bioconductor)](http://www.bioconductor.org/packages/release/bioc/html/trio.html)
- Features the function `getLD`
  - Inputs for `getLD` are genotypes {0, 1, 2}
  - Use `parentsOnly = TRUE` when not using Trio data

[SNPRelate (Bioconductor)](http://bioconductor.org/packages/devel/bioc/html/SNPRelate.html)
- Calculates `r` by EM algorithm assuming HWE.
- Features function `snpgdsLDMat`
  - Input is a `SNPGDSFileClass` object, an interface to Genomic Data Structure
  ([GDS](https://www.bioconductor.org/packages/devel/bioc/vignettes/gdsfmt/inst/doc/gdsfmt_vignette.html)) data files

[pink...](http://pngu.mgh.harvard.edu/~purcell/plink/)
An obvious choice that has been used previously in human studies utilizing
Affymetrix 500K SNP chips as seen [here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2896773/pdf/main.pdf).
Note that in that study, Plink was used to find correlations between genotypes,
not haplotypes. Also see this [study](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4021229/)
that looked at LD using the HD bovine chip.

[SNPPLD in gebv](https://www.researchgate.net/publication/267709544_gebv_Genomic_breeding_value_estimator_for_livestock)
Unsure where to download...
Used to estimate pairwise LD using BovineHD BeadChip data (~700K) as seen
[here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4243187/)

[Haploview](https://www.broadinstitute.org/haploview/downloads#JAR)
Another obvious choice. Importantly, can compute LD for any number of pairwise combinations of SNPs using `r^2`. Used in the
OvineSNP50 BeadChip for [sheep](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4659207/).
