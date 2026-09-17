# Compact matrix test dataset

This directory contains a reduced four-sample 10x matrix dataset for fast,
end-to-end validation of scHarbor matrix mode.

- Samples: `GSM9101188`, `GSM9101189`, `GSM9101191`, and `GSM9101192`
- Groups: two adult peripheral blood and two umbilical cord blood samples
- Cells: 250 per sample, 1,000 total
- Selection: 62 or 63 QC-passing cells from each of four broad immune
  lineages per sample: T cells, B cells, NK cells, and monocytes
- QC constraints: 200-5,000 detected genes, at least 700 UMIs, and no more
  than 10% mitochondrial counts
- Matrix format: gzipped 10x-compatible `matrix.mtx`, `features.tsv`, and
  `barcodes.tsv`

The full feature tables are retained so annotation, differential expression,
enrichment, trajectory, and CellChat modules can access their required genes.
The subset is intended only to verify software execution. It is not suitable
for biological inference, benchmarking accuracy, or reproducing published
cell-frequency estimates.

Selection counts and original matrix dimensions are recorded in
`subset_manifest.json`. Use `../samples.demo.tsv` as its matching metadata.
