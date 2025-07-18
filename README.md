# MeerKAT-pol

Pipeline:
https://github.com/AnnalisaB/MeerKAT-polarization/blob/main/MeerKAT_pol_script.py
At the moment, it is a CASA script, to be run inside CASA. If you want to flag, a singularity with AoFlagger installed is also needed
(LOFAR flocs at the moment)

# The following were used before but are not needed anymore
Pipeline singularity: `singularity build MeerKATpol.simg docker://tpasini/pol_meerkat:latest`
Tricolor singularity: `singularity build tricolour.simg docker://quay.io/stimela2/tricolour` 


#### Before running

Before running `MeerKAT_pol_script.py` you need to:
  1. run the script [correct_parang](https://github.com/bennahugo/LunaticPolarimetry/blob/master/correct_parang.py) for each field in your MS file; Script written by Ben Hugo and copied from  https://github.com/bennahugo/LunaticPolarimetry/blob/master/correct_parang.py
  2. split your MS into two files: `<MS>-CorrectPang-cal.MS` and `<MS>-CorrectPang-target.MS`; in the first one put all the calibrators and in the second one only the target field;
  3. create a directory 'MS_Files' and move your MS there.
