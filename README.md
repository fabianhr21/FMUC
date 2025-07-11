# FMUC
FMUC - Fast Modeling Urban Climate is a package developed in collaboration with the Barcelona Supercomputing Center and the Universitat Politècnica de Catalunya to model wind at urban scales using Neural Networks.
## Functionality
This repository is a guideline for generating urban climate wind analysis from Mesoscale Wheater Models and Urban Geometry.
## Pre-Process
In the Pre-Process directory, you can find scripts to prepare geometry from STL files to be processed by the Neural Network, the scripts are designed to obtain a georeferenced wind field and geometry at the end, so the best to use are BIM files which contain both geometry and georeference.

You can obtain BIM models from all of Catalunya on the following website:
https://geoportalcartografia.amb.cat/AppGeoportalCartografia2/index.html

And from all spain from: https://centrodedescargas.cnig.es/CentroDescargas/buscar-mapa

You can also use part of the City4CFD repository to generate CFD domains ready for simulation. This guideline can be used for traditional CFD solvers but this one is focused in preparing geometry for simulation with SOD2D, another repository developed by the Barcelona Supercomputing Center.

## Wind-NN
The Wind-NN uses a surrogate model to predict wind behavior, the output is a normalized wind field by components. More info about the model in the wiki.

## Post-Process
In the Post-Process section, you can find scripts to scale wind velocity and visualize.

# REQUIREMENTS
To use these tools pyAlya library is mandatory, developed by the Barcelona Supercomputing Center. You can ask for access to Arnau Miró <arnau.mirojane@bsc.es>

# USE
To test the base case you need to batch the RUN_WORKFLOW script.
Usage: sbatch ./RUN_WORKFLOW.sh stl_basename

