# ADOVAC_virome

This repository contains the code supporting all visualizations presented in the paper:

**The skin virome in acne vulgaris reveals increased orthototivirus diversity and three novel members of the *Orthototiviridae* family**

## Repository contents

- [`Acne_ADOVAC_virome.Rmd`](Acne_ADOVAC_virome.Rmd): fully executable R Markdown analysis that generates the visualizations.
- [`Acne_ADOVAC_virome.html`](Acne_ADOVAC_virome.html): rendered HTML version of the analysis.


## Reproducing the visualizations

1. Download the derived data associated with this repository from Zenodo:
2. Extract the downloaded files into the repository so that the directories are available under `data/` as shown below.
3. Open `ADOVAC_virome.Rproj` in RStudio or set the repository root as the working directory.
4. Install the R packages listed in the setup chunk of `Acne_ADOVAC_virome.Rmd` if they are not already installed.
5. Execute `Acne_ADOVAC_virome.Rmd` to reproduce the visualizations and analysis output.

## Derived-data structure

```text
data/
├── METADATA/
│   ├── ADOVAC_merged_virome_metadata.csv
│   └── ADOVAC_virome_metadata.csv
├── DE_NOVO_ASSEMBLY/
│   ├── INDIVIDUAL_SAMPLES/
│   │   ├── ABUNDANCES/
│   │   │   └── abundance_table.csv
│   │   ├── COUNTS/
│   │   │   ├── ADOVAC.number_raw_reads.txt
│   │   │   └── ADOVAC.number_trimmed_reads.txt
│   │   ├── PHAGE_ANNOTATION/
│   │   │   └── CHECKV/
│   │   │       └── quality_summary_R.tsv
│   │   └── VIRAL_CLASSIFICATION/
│   │       ├── BLASTN/
│   │       │   └── ADOVAC.blastn_against_hg38.txt
│   │       ├── DIAMOND/
│   │       │   └── ADOVAC.1000_contigs_95-85_diamond_taxonomy.csv
│   │       └── GENOMAD/
│   │           ├── All_samples_clustered_95-85_virus_scores.tsv
│   │           └── All_samples_clustered_95-85_virus_taxonomy.tsv
│   └── MERGED_SAMPLES/
│       ├── ABUNDANCES/
│       │   └── abundance_table_merged.csv
│       ├── COUNTS/
│       │   ├── ADOVAC_PID.number_Hostout_reads.txt
│       │   ├── ADOVAC_PID.number_raw_reads.txt
│       │   └── ADOVAC_PID.number_trimmed_reads.txt
│       ├── PHAGE_ANNOTATION/
│       │   ├── CHECKV/
│       │   │   └── quality_summary_R_merged.tsv
│       │   └── HOST_PREDICTION/
│       │       └── Host_prediction_to_genus_m90.csv
│       └── VIRAL_CLASSIFICATION/
│           ├── DIAMOND/
│           │   └── ADOVAC_merged.1000_contigs_95-85_diamond_taxonomy.csv
│           ├── GENOMAD/
│           │   ├── All_samples_clustered_95-85_virus_scores_merged.tsv
│           │   └── All_samples_clustered_95-85_virus_taxonomy_merged.tsv
│           ├── ORTHOTOTIVIRIDAE/
│           │   ├── ICTV_orthototiviridae_RdRps_with_outg.tsv
│           │   ├── all_orthototiviridae_with_outg.aln.fasta.treefile
│           │   └── complete_orthototiviridae_with_outg.aln_trimmed.fasta.treefile
│           └── VMR_MSL41.v1.20260320.xlsx
└── REFERENCE_GUIDED_ASSEMBLY/
    └── ESVIRITU/
        └── SUMMARY.detected_virus.info.tsv
```

## License

See [`LICENSE`](LICENSE).