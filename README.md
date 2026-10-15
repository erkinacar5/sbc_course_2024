# Spatial Biology of Cancer — R tutorials (2024)

Hands-on R tutorials from the **Spatial Biology of Cancer (SBC)** course at the Department of Biosystems Science and Engineering (D-BSSE), ETH Zurich, spring semester 2024.

Over three sessions the tutorials work through one human breast cancer sample, profiled with both single-cell and spatial transcriptomics. They go from single-cell annotation to spatial deconvolution and cell-type co-occurrence.

> A newer edition, with a ready-made Docker environment and a Visium HD session, is in [sbc_course_2026](https://github.com/erkinacar5/sbc_course_2026).

## Tutorials

| # | Date | Topic | Source | Rendered |
|---|------|-------|--------|----------|
| 0 | — | Setup: R/RStudio with `renv`, packages, data download | — | [HTML](https://erkinacar5.github.io/sbc_course_2024/00_setup_sboc_ss2024.html) |
| 1 | 24.04.2024 | **Single-cell analysis:** QC, normalization, clustering, marker genes, cell-type scoring with the 10x Xenium breast panel | [Rmd](01_sbc_240424_tutorial.Rmd) | [HTML](https://erkinacar5.github.io/sbc_course_2024/01_sbc_240424_tutorial.html) |
| 2 | 08.05.2024 | **Visium (1):** spatial QC, SCTransform, spatially variable genes, clustering, panel-based scoring on the tissue | [Rmd](02_sbc_240508_tutorial.Rmd) | — |
| 3 | 15.05.2024 | **Visium (2):** spot deconvolution with RCTD, composition clusters and cell-type co-occurrence with ISCHIA | [Rmd](03_sbc_240515.Rmd) | [HTML](https://erkinacar5.github.io/sbc_course_2024/03_sbc_240515.html) |

## Data

All datasets are public 10x Genomics FFPE human breast cancer samples (see the setup page for direct download links):

- [Chromium FFPE single-cell](https://cf.10xgenomics.com/samples/cell-exp/7.0.1/Chromium_FFPE_Human_Breast_Cancer_Chromium_FFPE_Human_Breast_Cancer/Chromium_FFPE_Human_Breast_Cancer_Chromium_FFPE_Human_Breast_Cancer_count_sample_filtered_feature_bc_matrix.h5): filtered feature–barcode matrix
- [CytAssist FFPE Visium](https://cf.10xgenomics.com/samples/spatial-exp/2.0.0/CytAssist_FFPE_Human_Breast_Cancer/CytAssist_FFPE_Human_Breast_Cancer_filtered_feature_bc_matrix.h5): filtered matrix plus the [spatial folder](https://cf.10xgenomics.com/samples/spatial-exp/2.0.0/CytAssist_FFPE_Human_Breast_Cancer/CytAssist_FFPE_Human_Breast_Cancer_spatial.tar.gz)
- [10x Xenium human breast gene panel](https://cf.10xgenomics.com/supp/xenium/panels/hBreast_v1.csv) (280 genes)

The cell-type annotation used for deconvolution comes from the original study: Janesick et al., *Nature Communications* (2023), [doi:10.1038/s41467-023-43458-x](https://doi.org/10.1038/s41467-023-43458-x).

## Running the tutorials

Tested with R 4.3.3 and RStudio 2023.12.1. Follow the [setup page](https://erkinacar5.github.io/sbc_course_2024/00_setup_sboc_ss2024.html) to create an `renv` project, then place the downloaded files in an `exercise_material/` folder next to the `.Rmd` files.

Main packages: [Seurat](https://satijalab.org/seurat/), [SeuratDisk](https://github.com/mojaveazure/seurat-disk), [spacexr (RCTD)](https://github.com/dmcable/spacexr), [ISCHIA](https://github.com/ati-lz/ISCHIA), tidyverse and patchwork.

## License

The tutorials are licensed under [CC BY 4.0](LICENSE): you can reuse and adapt them with attribution. The 10x Genomics datasets they use are covered by their own terms.
