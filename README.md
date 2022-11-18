# Quantum Variational Rewinding for Time Series Anomaly Detection

<div align="center">

<img src="https://raw.githubusercontent.com/AgnostiqHQ/covalent/master/doc/source/_static/covalent_readme_banner.svg" width=150%>

</div>

This repository contains an explicit code demonstration for the Quantum Variational Rewinding (QVR) algorithm as proposed in the article <https://arxiv.org/abs/2210.16438>

You will find:

1. A Jupyter notebook (`QVR_example.ipynb`) employing QVR to detect anomalous behaviour in cryptocurrency time series data (i.e, a local simulation of the cryptocurrency case in the article) and to detect anomalous behaviour in the synthetic univariate data from the article (i.e. the didactic toy example from the paper)

2. The pre-processed data sets used in the article in `~/data/`

## Install instructions

To run the Jupyter Notebook, you will need a new `conda` environment with all of the dependices.

First, clone or download this repository to your local machine.

Next, if you don't already have conda, navigate to <https://conda.io/projects/conda/en/latest/user-guide/install/download.html> and install the correct version for your OS for either Miniconda or Anaconda.

In a terminal window, navigate to root directory of this repo (`~QuantumVariationaRewinding`) and issue

`> conda env create -f environment.yml`

This will install the `QVR` environment. Let's activate it

`> conda activate QVR`

If you are confident with making this environment visible to your existing Jupyter Notebook viewer, you are done! If not, please continue with

`> python -m ipykernel install --user --name=QVR`

then issue

`> jupyter notebook &`

which will open a browser window in the Jupyter explorer. Navigate to the `QVR_example.ipynb` and click it.

From the top drop-down menu, select `kernel > change kernel > QVR`. You are now good to go!


### Start Covalent

After successfully creating the conda environment, the Covalent server can be started as follows

```bash
covalent start --ignore-migrations
```

Covalent can optionally be started in debug mode for more verbose logging as follows

```bash
covalent start -d --ignore-migrations
```
