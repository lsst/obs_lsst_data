This directory contains transmission curves for the LSSTCam filters at the location of each detector.
The transmission curves were derived by Andy Rasmussen based on scans from Materion at various positions and angles, and then interpolated and integrated for the LSSTCam beam.
Please see DM-46256 for details.

Data Processing
---------------

This directory contains the processed per-filter-per-detector files (integrated_transmission_materion_[band]band.fits) which are input to the following script:
```
python $OBS_LSST_DIR/python/lsst/obs/lsst/script/write_lsstcam_transmission_filter_detector.py
```
