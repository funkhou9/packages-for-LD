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
