This directory contains baseline filter transmission curves for the LSSTComCam instrument.
We do not have specific filter scans for the LSSTComCam filters, so the data for the curves are from version 1.9 of the [LSSTCam baseline u, g, r, i, z, y filter files in the throughputs repo](https://github.com/lsst/throughputs/tree/1.9/baseline).

Data Processing
---------------

To generate these files, one clones a local copy of the [throughputs
repo](https://github.com/lsst/throughputs), checks out version 1.9,
and sets up the repo with eups:
```
git clone https://github.com/lsst/throughputs.git
cd throughputs
git checkout 1.9
setup -r . -j
```
In the obs_lsst package, one then runs the script to write the files
using the througputs data:
```
python ${OBS_LSST_DIR}/python/lsst/obs/lsst/script/write_comcam_filter_files.py
```
