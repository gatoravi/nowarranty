# nowarranty

A personal toolbox of scripts for running genomics tools on HPC clusters,
collected over several years of work on human genetics and cancer genomics at
Washington University in St. Louis: the Conrad lab (Center for Genome
Sciences) and the McDonnell Genome Institute (MGI).

As the name says, these come with no warranty. They are working notes rather
than a polished package: each script records how a tool was actually run on
real data, and many have hard-coded paths. They are shared as a reference for
anyone setting up similar pipelines.

## What's inside

| Folder | Contents |
| --- | --- |
| [`DNGpaper/`](DNGpaper) | Analysis scripts for the DeNovoGear paper ([Ramu *et al.*, *Nature Methods* 2013](https://doi.org/10.1038/nmeth.2611)): running DeNovoGear on whole-genome and exome trios, comparing calls between callers, and ROC curves |
| [`Bash/`](Bash) | Cluster job wrappers: BWA alignment, BAM-to-BCF conversion, DeNovoGear runs per chromosome and as job arrays |
| [`SamTools/`](SamTools), [`Picard/`](Picard), [`GATK/`](GATK) | Read processing and QC: mpileup, duplicate marking, read groups, indel realignment, depth of coverage |
| [`VarScan/`](VarScan), [`DINDEL/`](DINDEL) | Small-variant and indel calling |
| [`Annovar/`](Annovar), [`GEMINI/`](GEMINI) | Variant annotation and querying |
| [`HapMix/`](HapMix) | Local ancestry inference in admixed genomes from HapMap data |
| [`Integrate/`](Integrate) | Summaries of gene-fusion calls from INTEGRATE |
| [`Genome/`](Genome) | MGI Genome Modeling System helpers for clinical sequencing (ClinSeq) cases: SNV/indel plots, validation-rate comparisons, SciClone output comparisons |
| [`IGV/`](IGV) | Batch scripts to generate IGV screenshots for reviewing variant calls |
| [`R/`](R) | Fitting binomial, beta-binomial and Poisson models to allele read counts, with model-fit plots |
| [`Python/`](Python), [`Perl/`](Perl) | Annotation of de novo calls, demultiplexing, file-format conversion, dbGaP download |
| [`Tex/`](Tex), [`Misc/`](Misc) | Figure assembly and one-off utilities |

## Related tools

- [DeNovoGear](https://github.com/ultimatesource/denovogear): de novo mutation
  calling in families
- [DNG_BetaBinomial_Paired](https://github.com/gatoravi/DNG_BetaBinomial_Paired):
  beta-binomial paired-sample caller (uses the R fitting code here)
- [regtools](https://github.com/griffithlab/regtools): regulatory variant
  analysis from DNA and RNA sequencing, developed at MGI
