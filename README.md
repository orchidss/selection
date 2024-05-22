# ORCHIDSS Sample Selection

This repository contains the code for producing the ORCHIDSS target selection. The repository is organized as follows:

- `Notebooks/`: Jupyter notebooks for producing the target selection
- `ETC_Templates/`: ETC templates for the ORCHIDSS targets
- `InputCatalogues/`: Optical, photometric and radio catalogues (and images) used for the target selection. Note that due to the GitHub file size limitations the catalogues themselves are not included in this repository. In future, the links to the public locations of these files when published will be included in this README for completeness.

## ORCHIDSSwideMFS

The `ORCHIDSSwideMFS` target selection is based on the Legacy DR8 optical photometry and GPz photometric redshifts (Duncan 2022). The optical selection requires the following criteria:
- Integrated redshift probability from GPz - $\int_{0}^{0.57}P(z)\text{d}z > 0.8$. And then either
    - Star-forming galaxy based on UVJ rest-frame colours and $M_B < M_{B}^{*}(z) + 0.7$ from Eazy fits fixed to the the GPz photometric redshift. Or...
    - $m_{r} < 19.5$ (i.e. a DESI BGS/GAMA like magnitude selection)  

Sample selection and catalogue generation is presented in this notebook:
- [MFS Selection Notebook](https://github.com/orchidss/selection/blob/main/Notebooks/oWIDE_MFS_sample_selection.ipynb): Jupyter notebook for producing the ORCHIDSSwideMFS target selection

## ORCHIDSSwideDDF

The `ORCHIDSSwideDDF` target selection is based on the Legacy DR8 optical photometry and GPz photometric redshifts (Duncan 2022), with radio selection based on the MIGHTEE DR1(2) catalogues and mosaic. The selection requires the following criteria:
- Optical: ntegrated redshift probability from GPz - $\int_{0}^{0.57}P(z)\text{d}z > 0.8$.
- Radio: MIGHTEE DR1(2) flux >15uJy and SNR > 3 (from either forced measurements of matches to the catalogue within 1.5")

Sample selection, catalogue generation and validation are presented in these notebooks:
- [WD02/XMM-LSS Selection](https://github.com/orchidss/selection/blob/main/Notebooks/oWIDE_XMM-LSS_sample_selection.ipynb)
- [WD03/CDFS Selection](https://github.com/orchidss/selection/blob/main/Notebooks/oWIDE_CDFS_sample_selection.ipynb)
- [WD10/COSMOS Selection](https://github.com/orchidss/selection/blob/main/Notebooks/oWIDE_COSMOS_sample_selection.ipynb)
- [Merging and validation](https://github.com/orchidss/selection/blob/main/Notebooks/oWIDE_DDF_MergingValidation.ipynb)

## ORCHIDSSdeep

The `ORCHIDSSdeep` target selection is based on the WAVES DDF optical photometry and photometric redshift catalogues, with radio selection based on the MIGHTEE DR1(2) catalogues and mosaic. The selection requires the following criteria:
- Optical: Integrated redshift probability from WAVES - $\int_{0}^{1.4}P(z)\text{d}z > 0.8$ and a magnitude limit of $m_{Z} < 22.8$
- Radio: MIGHTEE DR1(2) flux >15uJy and SNR > 3 (from either forced measurements of matches to the catalogue within 1.5")

Sample selection, catalogue generation and validation are presented in this notebook:
- [Deep Selection and Validation](https://github.com/orchidss/selection/blob/main/Notebooks/oDEEP_Selection_and_Validation.ipynb)