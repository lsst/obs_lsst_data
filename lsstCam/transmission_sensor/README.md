This is the location for the ecsv files that hold the QE curves

Updated Data
============

For DM-40164, Aaron Roodman went through the single raft data, and fixed several problems in the data used for the sensor transmission curves:

For 4 Rafts the SLAC single raft data had only 6 wavelengths, not the 30 or 36 wavelengths from all other CCDs.
For these rafts he used BNL good run data,
There was 1 amp with NAN values, since the channel was non-functional during single raft testing.
For this channel he took values from the mean the other amplifiers.
For 3 amps the signal raft values clearly have problems, with values at 0 or under 30% in g,r,i bands.
2/3 were channels with problems during the single raft testing.
These 3 channels are all currently functional.
For these he took values from the average of the other good amp values.
Both BNL and SLAC single raft data have anomalously high QE values at 1075 and 1100 nm, compared to the expected level from Si absorption.
He used the known Si absorption curves, coded up by Steve Ritz.
So for all channels he adjusted the QE just at 1075 and 1100 nm from the theoretical QE curve, normalized to the measured values at 750nm.

The parquet file in this directory was copied from https://github.com/aaronroodman/lsstcam-notebooks/blob/main/Raft/qe_raft_allvalues_nircorrected_20230725.parquet as part of this ticket.

The following table shows the source of data for each of the rafts:

| Row |	rtmid   | bay | runnum | location |
-------------------------------------------
| 0   | RTM-005 | R23 | 11852  | SLAC     |
| 1   | RTM-006 | R14 | 11746  | SLAC     |
| 2   | RTM-007 | R31 | 11903  | SLAC     |
| 3   | RTM-008 | R34 | 11952  | SLAC     |
| 4   | RTM-009 | R12 | 11415  | SLAC     |
| 5   | RTM-010 | R03 | 12139  | SLAC     |
| 6   | RTM-011 | R01 | 10861  | SLAC     |
| 7   | RTM-012 | R30 | 11063  | SLAC     |
| 8   | RTM-013 | R02 | 10982  | SLAC     |
| 9   | RTM-014 | R20 | 10928  | SLAC     |
| 10  | RTM-015 | R32 | 7678   | BNL      |
| 11  | RTM-016 | R24 | 12027  | SLAC     |
| 12  | RTM-017 | R03 | 8872   | BNL      |
| 13  | RTM-018 | R42 | 12120  | SLAC     |
| 14  | RTM-019 | R13 | 11808  | SLAC     |
| 15  | RTM-020 | R11 | 9442   | BNL      |
| 16  | RTM-021 | R41 | 12086  | SLAC     |
| 17  | RTM-022 | R43 | 11671  | SLAC     |
| 18  | RTM-023 | R10 | 10517  | SLAC     |
| 19  | RTM-024 | R22 | 11351  | SLAC     |
| 20  | RTM-025 | R21 | 10238  | BNL      |
-------------------------------------------
