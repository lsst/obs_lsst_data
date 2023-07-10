This directory contains an approximate mirror reflectivity curve for the Rubin Auxiliary Telescope.

Data Processing
---------------
Approximately every week, the Auxiliary Telescope mirror reflectivity is measured at 7 wavelengths, as recorded at https://confluence.lsstcorp.org/display/LTS/Aux+Tel+Reflectivity+Status.
These measurements are summarized in an Excel worksheet, "M1_Aux_Tel_R_2023_05_29xlsx.xlsx", a version of which (downloaded June 2023) is committed to this repo.
The values were exported by hand to a CSV file, "auxtel_mirror_052923.csv", also committed to this repo.

The sampling of the reflectivity data is limited, particularly in the z-band, where mirror chromaticity changes relatively rapidly as a function of wavelength.
The Subaru M1 mirror has a similar aluminum coating as AuxTel M1, and the reflectivity of this mirror is measured regularly to high precision and accuracy, and recorded at https://www.naoj.org/Observing/Telescope/Parameters/Reflectivity/#m1.
Visual inspection shows that the AuxTel mirror reflectivity at the 7 sampled wavelengths is on average consistent with the Subaru mirror as scanned on 19 Feb, 2020.
The file "subaru_m1_r_20200219.txt" was retrieved from https://www.naoj.org/Observing/Telescope/Parameters/Reflectivity/subaru_m1_r_20201209.txt on 10 July 2023, and then edited to remove some erroneous spaces that made it so Astropy was unable to read it properly, as well as the second measurements between 950 and 1000 nm.

The final mirror transmission used as the AuxTel baseline is then taken as the Subaru M1 measurement from 19 February, 2020, and adjusted by 3.5% to match the average of the AuxTel throughput measurements over 3 years of measurements.
The chromatic shape of the mirror transmssion recorded in this repo is then consistent with the average AuxTel measurements, but at higher resolution, including the complex shape of the reflectivity of aluminum around 800 nm that are not captured in the AuxTel scans.
For calibration purposes, the chromatic shape of the mirror reflectivity is much more important than the absolute throughput which is degenerate with numerous other effects.

Note that this file only contains reflectivity from AuxTel M1, and not from any of the other optical elements.

The file was converted to the calib format by running the script `python $OBS_LSST_DIR/python/lsst/obs/lsst/script/rewrite_latiss_optics_file.py`.
