# JWST MIRI Spectral Analysis: NGC 7469

This repository holds the code and extracted data from my 120-hour Data-Driven Astronomy internship. I used JWST MIRI IFU data to extract and compare mid-infrared spectra from the Seyfert 1 galaxy NGC 7469.

### The Science
I wanted to map the physical differences between the AGN-dominated galactic center and the star-forming ring around it. The extracted spectra clearly show AGN photoionization signatures (strong [S IV] and [Ne VI] lines) in the center, while the ring is dominated by PAH emission and warm molecular hydrogen (H2) lines typical of starburst regions.

### Repo Notes
The raw Level-3 `s3d.fits` data cubes from the MAST archive are too large to host on GitHub. Instead, I've included:
*   The extracted, rest-frame corrected spectra in `data/` as CSVs.
*   My Jupyter notebook (`scripts/`) used for masking, extraction, and peak detection.
*   The final 4-page scientific report and my internship certificate in `docs/`.

Requires `astropy`, `regions`, `pandas`, `numpy`, and `matplotlib`.
