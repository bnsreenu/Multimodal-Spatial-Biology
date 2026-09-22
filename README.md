# Multimodal Spatial Biology

Companion notebooks for the DigitalSreeni YouTube series on multimodal spatial biology: combining tissue morphology (H&E), multiplexed protein imaging (COMET), and spatial transcriptomics (Xenium) on the same tissue sections to answer real biological questions.

## About this series

Each episode builds on the last, starting from raw image loading and working up to unsupervised cell typing, spatial statistics, and a four tissue type atlas. No modality is treated as more important than another: H&E, COMET, and Xenium each contribute something the others cannot.

## Episodes

| # | Title | Notebook |
|---|---|---|
| 1 | Introducing the dataset | `Video1_unumlocalia_intro.ipynb` |
| 2 | Registration | `Video2_unumlocalia_registration.ipynb` |
| 3 | Segmentation and per cell quantification | `Video3_unumlocalia_segmentation.ipynb` |
| 4 | A real biological result | `Video4_unumlocalia_biological_result.ipynb` |
| 5 | Tumor versus non tumor comparison | `Video5_unumlocalia_tumor_vs_normal.ipynb` |
| 6 | Cross modality validation | `Video6_unumlocalia_cross_modality_validation.ipynb` |
| 7 | Unsupervised clustering | `Video7_unumlocalia_unsupervised_clustering.ipynb` |
| 8 | Spatial neighborhood analysis | `Video8_unumlocalia_spatial_neighborhood.ipynb` |
| 9 | What only Xenium can show us | `Video9_unumlocalia_xenium_exclusive_biology.ipynb` |
| 10 | Protein and transcript, a systematic comparison | `Video10_unumlocalia_systematic_concordance.ipynb` |
| 11 | Cell to cell spatial interaction | `Video11_unumlocalia_cell_interaction.ipynb` |
| 12 | Morphology versus molecular identity | `Video12_unumlocalia_morphology_vs_molecular.ipynb` |
| 13 | A four core atlas | `Video13_unumlocalia_four_core_atlas.ipynb` |

## Dataset

This series uses the UnumLocalia dataset from Duchini, Marsh-Wakefield, et al., four tissue microarray cores (hepatocellular carcinoma, non tumor liver, tonsil, and hepatocellular adenoma), each with paired H&E, COMET (16 protein markers), and Xenium (5,001 gene panel) data on the same physical section.

- Paper: bioRxiv, 2026 — https://www.biorxiv.org/content/10.64898/2026.08.17.742355v1
- Data: Zenodo, CC BY 4.0 — https://zenodo.org/records/21713660
- Original code: https://github.com/Felixillion/UnumLocalia, MIT license

Full credit to the original authors for making this data openly available. This repository does not redistribute the dataset itself; download it from Zenodo and place it under `data/UnumLocalia` to run these notebooks.

## Setup

```bash
conda create -n unumlocalia-env python=3.10
conda activate unumlocalia-env
pip install numpy pandas pyarrow scipy scikit-image scikit-learn tifffile zarr shapely pillow matplotlib napari scanpy python-igraph leidenalg harmonypy
pip install -e path/to/UnumLocalia --no-deps
```

Each notebook saves its outputs (figures and intermediate CSVs) into its own `outputs/videoN` folder.

## License

Code in this repository is shared for educational purposes. The underlying dataset remains subject to its original CC BY 4.0 license from the source authors.

## More

Full video walkthroughs available on DigitalSreeni — https://www.youtube.com/@DigitalSreeni
