This directory contains baseline optics transmission curves for LSSTCam.
As we do not currently have specific scans of the instrument, the data for the curves are from version 1.9 of the [LSSTCam baseline files `m1.dat`, `m2.dat`, `m3.dat`, `lens1.dat`, `lens2.dat`, `lens3.dat` in the throughputs repo](https://github.com/lsst/throughputs/tree/1.9/baseline).

Data Processing
---------------

To generate the transmission optics file, one clones a local copy of
the [throughputs repo](https://github.com/lsst/throughputs), checks
out version 1.9, and sets up the repo with eups:
```
git clone https://github.com/lsst/throughputs.git
cd throughputs
git checkout 1.9
setup -r . -j
```
In the obs_lsst package, one then runs the script to write the files
using the throughputs data:
```
python ${OBS_LSST_DIR}/python/lsst/obs/lsst/script/write_lsstcam_transmission_optics.py
```
That script multiplies together the throughputs for the six mirror and
lens componnents of the telescope and writes the result to a single
transmission_optics file.
