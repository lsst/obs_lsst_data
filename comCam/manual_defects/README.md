This directory contains manual defects for the LSSTComCam instrument.

The defects are a combination of manually identified phosphorescent regions, warm corners, and other column features that are not currently captured by the defect finding code.

Data Processing
---------------

The manual defects were generated by running:
```
python $OBS_LSST_DIR/python/lsst/obs/lsst/script/write_comcam_manual_defects.py
```

The output files then have to be edited by hand to set INSTRUME to "ComCam" instead of "LSSTComCam".
