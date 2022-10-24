This directory contains filter transmission curves for the 65mm LATISS
filters, with measurements and processing as described below.

Data Processing
---------------

The data in this directory have been extracted from a spreadsheet of
values provided along with the email description of how the scans were
performed.  After converting the spreadsheet to a CSV file, columns
H-J,L-U were extracted.  The two measurements in the SDSSu_65mm~empty
band were averaged together.  No normalization using column K
performed in this band, as those values were all consistent with
unity, and similar data is not available for the other bands.

No negative values were clipped in any band, although they were likely
caused by random noise during measurement.  For consistency with other
transmission curves in this package, the wavelengths were converted to
nanometers.


Subject: Baader SDSS Filters
----------------------------

From: Dick Joyce
Sent: Wednesday, April 13, 2022 9:49 PM
To: Patrick Ingraham; Gary Poczulp; Ron Harris

I was able to pick up the LSST filters from Ron Harris today and measure them on
the Lambda9 (which thankfully was still working after a >2 year hiatus).  The
Lambda9 works pretty well for a 35 year old spectrometer which was last
refurbished in 2011, with only one problem--one of the grating drives which
switches between the UV/visible and IR gratings does not work, so I have to
manually rotate the grating stage.  As a result, I had to make the measurements
in two separate stages: from 300 to 860 nm and 870 to 1250 nm (the crossover
point is 868 nm), so there is a gap of 10 nm in the data.

For each of the two regions, I followed the same procedure:

1.  Put in a sample of glass doped with Holmium Oxide which has several sharp
absorption features to check the wavelength calibration.  For both the
UV/visible and IR, the results matched the calibration to within 0.1 nm

2.  With no filter in the beam, run a "background" scan which internally sets
the transmission to 100% for each wavelength.

3.  With the filter in the beam, run a "leak" scan at a fairly high rate
(240 nm/min) over the entire span of the region.

4.  Run a second "bandpass" scan at a lower rate (60 nm/min) over the filter
bandpass with a little margin on the ends.

Fortunately, those scans which spanned the 868 nm transition appear to have done
so with no obvious jumps, so the background compensation worked pretty well.

Gary noted that these filters have a preferred orientation.  I figured this out
by looking for internal reflections in the filter and aligning the filter so the
beam passed through the side without these internal reflections.  Later, Gary
told me that the edge blacking very slightly masks this side and provides an
easier clue.  Just for completeness, I measured the u' filter from both
directions and, as expected, saw no difference between the two scans.

u' filter:  As noted above, the two filter scans from either side were virtually
identical.  I was initially surprised by the very sharp cuton at 325 nm and
feared there might be a problem with the UV light source, but a succeeding scan
with no filter showed a very nice 100% over the filter scan range, alleviating
my concerns.  I saw no out of band leaks to 1250 nm

The g', r',  i' , and z' filters all have nice profiles with good transmission
but all have long wavelength leaks beyond about 1100 nm. This should be beyond
the cutoff wavelength of most CCDs, unless one is using a very deep depletion
detector.

The y' filter has no out of band leaks.

The IR scans will be a little noisier than the UV/visible because of the
sensitivity of the PbS IR detector, which is actually loses sensitivity as one
approaches the short wavelength end of the IR region.
