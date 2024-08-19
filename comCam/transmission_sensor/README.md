This directory contains baseline sensor QE curves for the LSSTComCam instrument.
The LSSTComCam focal plane consists of one raft of ITL sensors.
As we do not have QE scans of LSSTComCam, we have simply taken an average of all the ITL sensors from the LSSTCam sensor QE scans as processed in DM-40164.

Data Processing
---------------

To generate these files, you run this script from obs_lsst.
```
python python/lsst/obs/lsst/script/write_comcam_estimated_transmission_sensor.py
```
