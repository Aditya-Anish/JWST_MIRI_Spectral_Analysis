# JWST MIRI Spectral Analysis: NGC 7469

This repository contains a Python-based observational astrophysics pipeline developed to extract and analyze mid-infrared spectra from the James Webb Space Telescope (JWST). This project was completed as part of a 120-hour Data-Driven Astronomy internship with the India Space Academy.

## Scientific Objective

The primary goal of this project is to analyze the mid-infrared emission features of the Seyfert 1 galaxy **NGC 7469**. By processing level-3 Integral Field Unit (IFU) data cubes from JWST's MIRI instrument (Channels 1-4), the pipeline extracts and compares the spectra from two distinct physical environments:
* **The Center Region:** The AGN-dominated galactic nucleus.
* **The Ring Region:** The surrounding circumnuclear star-forming ring.

## Key Astrophysical Findings

By comparing the extracted spectra across the 5 to 28-micron range, the data reveals distinct ionization mechanisms:
* **AGN Signatures (Center):** Shows strong high-ionization fine-structure lines like [S IV] (10.51 microns) and [Ne VI] (7.65 microns), consistent with AGN photoionization.
* **Star Formation Signatures (Ring):** Exhibits significantly enhanced Polycyclic Aromatic Hydrocarbon (PAH) emission (7.7, 8.6, and 11.3 microns) and warm molecular hydrogen lines (H2), which are classic tracers of active star-forming regions.

## Repository Structure

* **`data/`**: Contains the extracted, rest-frame corrected spectral data (`.csv`) and the DS9 region configuration file. *(Note: Raw JWST `s3d.fits` data cubes are excluded from this repository due to GitHub size constraints).*
* **`scripts/`**: Contains the core Jupyter Notebook (`JWST_MIRI_spectra_analysis.ipynb`) used for WCS coordinate transformations, spatial masking, flux extraction, and automated peak detection.
* **`output/`**: Contains the generated spectral plots comparing the Center and Ring regions across all MIRI channels.
* **`docs/`**: Includes the final 4-page scientific report and official internship certification.

## Dependencies

The analysis pipeline requires Python and the following standard astronomical libraries:

```bash
pip install astropy pandas numpy matplotlib regions scipy
