# MLCCS_GenSmooth

This repository holds install instructions and a practice script - allowing you to estimate the models discussed during the
"General Smooth Models for the Cognitive Sciences" lecture, which is part of the ML for CCS course at the RUG.

To estimate the models we make use of ``mssm`` - a toolbox to estimate Generalized Additive Mixed Models (GAMMs),
Generalized Additive Mixed Models of Location Scale and Shape (GAMMLSS), and more general (mixed) smooth models in the sense defined
by [Wood, Pya, & Säfken (2016)](https://doi.org/10.1080/01621459.2016.1180986). Approximate estimation (and automatic regularization) of the latter only requires users to provide the (gradient of) the log-likelihood. Furthermore, ``mssm`` is an excellent choice for the modeling of multi-level time-series data, often estimating additive models with separate smooths for thousands of levels in a couple of minutes. **Documentation** for ``mssm`` is hosted [here](https://jokra1.github.io/mssm/index.html)

**Note**: The ``practical.ipynb`` file contains the practice notebook (for the practical it is recommended that you use [Visual Studio Code](https://code.visualstudio.com)
as your IDE. It is also recommended that you install the ``Python`` and ``Jupyter`` extensions - see [here](https://code.visualstudio.com/docs/editor/extension-marketplace)
for instructions on how to do that in VSC.). A link to the data will be shared during the practical. Before you can start working with the notebook, a couple of python packages
will have to be installed!

## Installation

First [clone](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) the repository, so that you have it available on your machine. If you have ``git`` installed on your machine, simply open a terminal, navigate to the folder that you want to contain the files from this repository, and run:

```
git clone https://github.com/JoKra1/MLCCS_GenSmooth.git
```

If you don't have ``git`` installed on your machine, simply click on the green ``<> Code`` button at the top of this repository and ``Download ZIP``. Now we can install the required Python packages.

The easiest option to install the required packages is to get them directly from pypi via ``pip``. This can be achieved in two steps:

1) Setup a [conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) with python > 3.10
2) Install packages via ``pip``

To complete both steps, first install ``conda`` (if you don't have it already) - see [here](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html) for instructions. Then,
in an open terminal, simply run the following lines to install all packages required for the practical:

```
conda create -n mssm_env python=3.13
conda activate mssm_env
pip install mssm mssmViz numdifftools
```

Then you can start working through the ``practical.ipynb`` notebook. Make sure to select the ``conda`` environment you created in the last step as Kernel
in VSC (see [here](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) for a tutorial on working with ``Jupyter`` notebooks in VSC.). **Note**: VSC might inform you that
additional packages are required when working with ``Jupyter`` notebooks and will offer to install those - please do so.
