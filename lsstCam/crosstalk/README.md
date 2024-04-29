Crosstalk coefficients for LSSTCam, `c0` and `c1`. The latter is the non-linear term.
The coefficents were provided by Adam Snyder (UCDavis, as of 2024) from laboratory
spots measurements.
They are available in the Butler repository `/sdf/group/rubin/repo/main` at the USDF, in collections
`u/snyder18/13199/crosstalk_analysis/20240406T213728Z` (if detId < 99) and `u/snyder18/13198/crosstalk_analysis/20240406T214205Z`.
The script used to retrieve the coefficients from these collections and make the `ecsv` files here can be found in:
`$OBS_LSST_DIR/python/lsst/obs/lsst/script/write_non_linear_crosstalk_coeffs.py`
