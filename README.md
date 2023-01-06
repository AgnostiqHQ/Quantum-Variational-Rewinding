# Quantum Variational Rewinding for Time Series Anomaly Detection

<div align="center">

<img src="https://raw.githubusercontent.com/AgnostiqHQ/covalent/master/doc/source/_static/covalent_readme_banner.svg" width=150%>

</div>


Author: Jack S. Baker

Email: <research@agnostiq.ai>

This repository contains an explicit code demonstration for the Quantum Variational Rewinding (QVR) algorithm as proposed in the article <https://arxiv.org/abs/2210.16438>.

In this repository, you will find:

1. A Jupyter notebook (`QVR_example.ipynb`) employing QVR to detect anomalous behaviour in cryptocurrency time series data (i.e, a local simulation of the cryptocurrency case in the article) and to detect anomalous behaviour in the synthetic univariate data from the article (i.e. the didactic toy example from the paper)

2. The pre-processed data sets used in the article in `~/data/`

## Install instructions

The code in this repository supports Mac and Linux operating systems.

To run the Jupyter Notebook, you will need a new `conda` environment with all of the dependencies.

First, clone or download this repository to your local machine.

Next, if you don't already have conda, navigate to <https://conda.io/projects/conda/en/latest/user-guide/install/download.html> and install the correct version for your OS for either Miniconda or Anaconda.

In a terminal window, navigate to root directory of this repo (`~QuantumVariationaRewinding`) and issue:

```bash
conda env create -f environment.yml
```

This will install the `QVR` environment. Let's activate it:

```bash
conda activate QVR
```

Now we need to make sure this kernel is visible to the jupyter notebook:

```bash
python -m ipykernel install --user --name=QVR
```

then run:

```bash
jupyter notebook
```

which will open a browser window in the Jupyter explorer. Navigate to the `QVR_example.ipynb` and click it.

From the top drop-down menu, select `kernel > change kernel > QVR`. You are now good to go!

You should be able to run the notebook after starting the covalent server as mentioned below.


### Start Covalent

After successfully creating (and activating) the conda environment, the Covalent server can be started by entering the below command in a new terminal window:

```bash
covalent start --ignore-migrations
```

Covalent can optionally be started in debug mode for more verbose logging as follows:

```bash
covalent start -d --ignore-migrations
```

Once you're done, you can stop the server by doing:

```bash
covalent stop
```
