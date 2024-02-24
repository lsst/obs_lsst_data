This directory contains filter transmission curves for the simulated
ComCam LSSTComCam instrument, LSSTComCamSim.  The data for the curves
are from version 1.9 the of the [LSSTCam baseline g, r, i filter files
in the throughputs
repo](https://github.com/lsst/throughputs/tree/1.9/baseline).

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
python ${OBS_LSST_DIR}/python/lsst/obs/lsst/script/write_comCamSim_filter_files.py
```
