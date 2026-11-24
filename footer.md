# Description

DNA methylation at CpG sites is a central epigenomic modification with a broad
and diverse variety of functions across eukaryotes. DNA methylation involves a
covalent modification, can be directly replicated through cell division, is
often observed to be stable over long time periods, and is associated with known
pathways that enable regulatory dynamics. Within vertebrata, DNA methylation
tends to be associated with epigenomic repression of transcription, and the
simplest methylome features are hypomethylated valleys at promoters and
enhancers.

Methbase includes thousands of methylomes all analyzed with the same pipeline.
The Methbase tracks display a variety of methylome data and features.  All
tracks are based on sequencing data, and these include, for each methylome, a
"levels" track with the estimated methylation level at each CpG site, and a
"reads" track to indicate the amount of data informing each
estimate. Additionally, the following methylome features are included as
appropriate for the species, the cell type and the data characteristics:
hypomethylated regions (HMR), partially methylated domains (PMD), and
allele-specific methylated regions (AMR).

# Display Conventions and Configuration

The HMR, PMD, and AMR region calls are presented as BED blocks in tracks
associated with each experimental sample. The read counts and percentage of
methylated reads are also presented for reference as bigWig graphs.  See the
References section for explanations of methods behind each track.

# Methods

Methbase collects publicly available whole-genome bisulfite sequencing runs
from the NCBI Sequence Read Archive and reprocesses all of them through one
uniform pipeline built on DNMTools. Reads are mapped with abismal, duplicates
are removed, the bisulfite conversion rate is estimated, and per-site
methylation levels are computed and symmetrized across the two strands of each
CpG. A methylome enters the browsable collection only if its bisulfite
conversion rate is at least 0.9 and at least 70% of CpG sites are covered, which
in practice implies well above 1x average coverage.

This track hub is made from the data in Methbase at USC by the Smith Lab and
mirrored locally for faster access.

# Data Access

The data can be explored interactively in table format with the Table Browser or
the Data Integrator and exported from there to spreadsheet or tab-sep tables.
From scripts, the data from individual tracks can be accessed through our API,
but identifying specific subtracks from the thousands available may be difficult
without the faceted interface presented here.

# Credits

Thanks to Andrew D. Smith and the Smith lab at the University of Southern
California for building Methbase and for making these analyses available. The
collection is maintained at: https://github.com/smithlabcode/methbase Please use
"Issues" at that github repo to ask questions about the data and methods or
contact Andrew directly.

# References

Original Methbase:

Song Q, Decato B, Hong EE, Zhou M, Fang F, Qu J, Garvin T, Kessler M, Zhou J,
Smith AD (2013). A reference methylome database and analysis pipeline to
facilitate integrative and comparative epigenomics. PLoS One,
8(12):e81148. PMID: 24324667; PMC: PMC3855694

Bisulfite read mapping:

De Sena Brandine G, and Smith AD (2021).  Fast and memory-efficient mapping of
short bisulfite sequencing reads using a two-letter alphabet.  NAR Genomics and
Bioinformatics, 3(4), p.lqab115.  PMID: 34988438; PMCID: PMC8693577

HMRs:

Molaro A, Hodges E, Fang F, Song Q, McCombie WR, Hannon GJ and Smith AD (2011).
Sperm methylation profiles reveal features of epigenetic inheritance and
evolution in primates.  Cell, 146(6):1029-1041. PMID: 21925323; PMCID:
PMC3205962

AMRs:

Fang F, Hodges E, Molaro A, Dean M, Hannon GJ, Smith AD (2012). Genomic
landscape of human allele-specific DNA methylation. PNAS, 109(19):7332-7. PMID:
22523239; PMC: PMC3358917

PMDs:

Decato BE, Qu J, Ji XJ, Wagenblast E, Knott SRV, Hannon GJ, and Smith AD (2020).
Characterization of universal features of partially methylated domains across
tissues and species.  Epigenetics & Chromatin 13,.1:1-14. PMID: 33008446; PMCID:
PMC7532633

Pipeline components (DNMTools):

Andrew D. Smith (2026). https://github.com/smithlabcode/dnmtools

# Column headings

- accession: Experiment accession for the corresponding record in SRA. This is
  the primary key identifying each methylome.
- tissue: Inferred tissue of origin for the methylome based on metadata from the
  corresponding SRA sample.
- cancer status: (present for hg38 and mm39) Inferred cancer status for the
  methylome based on metadata from the corresponding SRA sample.
- cultured: (present for hg38 and mm39) Inferred status as a cell line or
  cultured sample for the corresponding SRA sample.
- strain: (present for mm39) Inferred strain label for the methylome based on
  metadata from the corresponding SRA sample.
- study: Study accession in SRA for the given methylome.
- sample: Sample accession for the corresponding experiment record in SRA.
- bsrate: Estimated bisulfite conversion rate based on non-CpG cytosines. Any
  non-CpG cytosine methylation will reduce this estimate.
- meth: Weighted global mean methylation level.
- depth: Mean number of reads informing each CpG site.
- mapping: Fraction of reads that map uniquely to the reference genome. In the
  case of paired-end reads, if pairs do not map concordantly the ends are then
  mapped independently and but this value reflects concordant pairs.
- uniq: Fraction of uniquely mapped reads that are not identified as duplicates,
  determined by identical mapping positions.
- sites: Fraction of CpG sites covered at least once by uniquely mapped reads.
- hmr size: mean size of identified HMRs.
- hmr count: number of identified HMRs.
- amr size: mean size of identified AMRs (AMRs are not identified in germ cells,
  cancers, cell lines, or methylomes with less than 8x coverage or less than 0.5
  global methylation).
- amr count: number of identified AMRs.
- pmd size: mean size of identified PMDs (only identified in hg38 and mm39).
- pmd count: number of identified PMDs.
