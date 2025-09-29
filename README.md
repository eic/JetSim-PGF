This repository houses codes for generating photon-gluon fusion process with Pythia 6.428, as such process can not be simulated by Pythia8. 

The Pythia 6.428, tuned to HERA data, is used. See: https://gitlab.com/eic/mceg/PYTHIA-RAD-CORR. 

To run the code on RCF, follow: 
```
setenv EIC_LEVEL EIC2022a
source /cvmfs/eic.opensciencegrid.org/gcc-8.3/MCEG/releases/etc/eic_cshrc.csh
pythia-eic < pgf.pythia6.18x275.noRC.txt
```

The running card ``pgf.pythia6.18x275.noRC.txt`` is adjusted to produce both photon+gluon and photon+quark processes in 18x275 ep collisions with Q2 > 1. 

Output files are then processed with eic-smear and afterburner, both available within eic-shell, for further simulation and reconstruction.
