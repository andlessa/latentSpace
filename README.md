# latentSpace
code and data sets for the latent space project


## Data Sets

The MC event data sets can be downloaded [here](https://cernbox.cern.ch/s/1cgCJ8JdQjCfYou) and include:

 * A DM simplified model with a pseudoscalar mediator (DMSimp_pseudoscalar_all.tar.gz)
 * A DM simplified model with a vector mediator (DMSimp_vector_all.tar.gz)
 * Associated squark-neutralino production (squarkMonojet.tar.gz)   

## Reproducing the data sets

In order to reproduce the data sets, the following external tools are needed:

  * [MadGraph5](https://launchpad.net/mg5amcnlo) with [Pythia8](https://pythia.org/) and [Delphes](https://cp3.irmp.ucl.ac.be/projects/delphes)

Running:

```
./installer.sh
```

should install MadGraph with the needed external packages.

Once MadGraph has been installed, running:

```
./runScanMG5.py -p <scan_parameters>
```

should run MadGraph5 over a range of model parameters and generate events for each set of values.
The following parameters files can be used to reproduce the datasets:

 * [scan_parameters_pseudoscalar.ini](./scan_parameters_pseudoscalar.ini): parameters for the DM simplified model with a pseudoscalar mediator
 * [scan_parameters_vector.ini](./scan_parameters_vector.ini): parameters for the DM simplified model with a vector mediator
* [scan_parameters_squarkMonojet.ini](./scan_parameters_squarkMonojet.ini): parameters for the squark DM associated production

The UFO models required to run the above scans are available in the [modelFiles](./modelFiles/) folder.

