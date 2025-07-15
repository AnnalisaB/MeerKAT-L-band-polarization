# MeerKAT-pol

Pipeline:
https://github.com/AnnalisaB/MeerKAT-polarization/blob/main/MeerKAT_pol_script.py

Pipeline singularity: `singularity build MeerKATpol.simg docker://tpasini/polarisation_workshop:latest`

Tricolor singularity: `singularity build tricolour.simg docker://quay.io/stimela2/tricolour`


#### Before running

Before running 'MeerKAT_pol_script.py' you need to run the script [correct_parang](https://github.com/bennahugo/LunaticPolarimetry/blob/master/correct_parang.py) for each field in your MS file.
After this, split your MS into two files: <MS>-CorrectPang-cal.MS and <MS>-CorrectPang-target.MS; in the first one put all the calibrators and in the second one only the target field.
Create a directory 'MS_Files' and move your MS there.
