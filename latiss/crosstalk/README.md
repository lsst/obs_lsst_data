Crosstalk coefficients for LATISS.
These were created by Chris Waters on DM-37819 and have been part of the default calibration collection.
The crosstalk coefficients are being transferred to here as a "curated calibration" to make sure they are always available for testing, as the new LSST ISR task assumes crosstalk matrices are always available.
The script to make these crosstalk tables can be run on USDF:
`python $OBS_LSST_DIR/python/lsst/obs/lsst/script/write_latiss_crosstalk_coeffs.py`
