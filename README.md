# packages-for-LD

> A list of existing software (preferably R packages) that include implementation
> to estimate genome-wide levels of linkage disequilibrium

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
not haplotypes.

[SNPPLD in gebv](https://www.researchgate.net/publication/267709544_gebv_Genomic_breeding_value_estimator_for_livestock)
Unsure where to download...
Used to estimate pairwise LD using BovineHD BeadChip data (~700K) as seen
[here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4243187/)
