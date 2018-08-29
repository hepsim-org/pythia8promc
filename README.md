# Pythia8ProMC

Interface of Pythia8 with ProMC
This is an example of how to interface Pythia8 Monte Carlo
generator with the [ProMC file format](https://atlaswww.hep.anl.gov/asc/promc/) for
[HepSim Monte Carlo repository](http://atlaswww.hep.anl.gov/hepsim/).
We use the VarintPacked particles method to fill particle records which gives very good file size
reduction.

It assumes that the following variables are set:

```
PROMC
PYTHIA8
CLHEP
ROOTSYS
```

Look at the Makefile. Generally, ROOT is not needed, but we keep it for some tests. 
In order to insert data models  (used to fill events), make sure your have a soft link "proto" to the directory
where proto files are  located.

After compiling the code, run the test job "A_RUN" which creates 10 ProIO files inside the directory "out"


S.Chekanov (ANL)
