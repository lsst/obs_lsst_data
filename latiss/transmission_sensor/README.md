This directory contains sensor QE curve for the LATISS sensor, ITL-3800C-068.

Data Processing
---------------
The input FITS file was downloaded from https://srs.slac.stanford.edu/DataCatalog/dataset.jsp?dataset=40352803&experiment=LSST-CAMERA which contains the Brookhaven National Lab Test Stand 3 (TS3) measurements of the sensor QE.

This was then converted to the calib format by running the script `python $OBS_LSST_DIR/python/lsst/obs/lsst/script/rewrite_latiss_qe_file.py`.

Both the original FITS and output ecsv files have been committed to this repo.
