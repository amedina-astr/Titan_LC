Lightcurve / Phase Curve Analysis Tools for Titan

This repository houses Jupyter notebooks and supporting code for analyzing Titan’s light curves, brightness phase curves, and polarization behavior from imaging data (e.g. from Cassini).

Overview & Goals:
- Provide a pipeline to go from raw image data (VICAR/IMG formats) to phase curves, polarization curves, and visual comparisons.
- Include deconvolution, image registration / alignment, brightness extraction, and polarization modeling steps.
- Serve as a tool for comparing observations to models of Titan’s atmosphere (clouds, scattering, haze).
- Allow scoring / statistical comparison of model predictions vs data.

You will want to install the following (or similar) dependencies to run the notebooks and support code:
- rms-vicar — for reading, manipulating, and processing VICAR / IMG formatted image
- opencv (cv2) — for general image processing: alignment, registration, filtering
- Optional: astropy, scikit-image, or others depending on your extended tools

Examples & Outputs
- Example brightness / phase curves for Titan in specific wavelength bands.
- Polarization-phase curves under varying assumptions of haze / scattering models.
- Residual plots showing data vs model differences.
- Score tables summarizing how well different models match the data.

You can open the notebooks and see embedded figures and code to guide reproduction.
