Work in progress: this is a module/recipe of open source software practices for authors of reproducible science publishing interactive code and educational materials. 

# Software Instructions: Online and Personal Computer


INTERACTIVE! You won't regret clicking on this badge. 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ChristinaB/Observatory/master)


To open interactive Jupyter Notebooks with Binder JupyterHub server. You will be connected to a virtual machine with the software environment required to execute the models.

## Online Modeling Instructions 

To open interactive Jupyter Notebooks with the CUAHSI JupyterHub server, go to the upper right corner of the resource page and click on 'Open With'. Select CUAHSI JupyterHub.  You will be connected to a virtual machine with the software environment required to execute the models.

Notebook 1: Learn about Observatory functions applied to Skookum Creek in the Nooksack Watershed. OGH_skookum_hybrid_2020417.ipynb

## Personal Computer Installation Instructions 

### Packages

The notebooks included in this resource require the following Python 3 packages:

```
geopandas==0.5.0

dask==1.2.0

hs_restclient==1.3.5

hstools==0.0.1

descartes==1.1.0

landlab==1.10.0  


```

To ensure that you have the correct packages and versions, run the following command(s) inside a Python terminal:

```
$ conda list
```

or 

```
$ pip list
```

### Creating a Working Environment

We recommend using Anaconda to create a fresh Python environment with all dependencies installed. After installing Anaconda, simply run the commands below with your desired environment name in place of `MY_ENVIRONMENT_NAME`:

```
conda create -n MY_ENVIRONMENT_NAME --file requirements.txt
```

activate the environment and start a jupyter server

```
source activate MY_ENVIRONMENT_NAME
jupyter notebook
```
### Debugging a Working Environment
Are you getting errors?  Here are some suggested steps. If you still have issues, email help@cuahsi.org or reach out to us (comment on this resource or see emails in HydroShare profiles) and we will invite you to the HydroShare Slack #landlab channel. 

Bug: PackagesNotFound

```
PackagesNotFoundError: The following packages are not available from current channels.
```

Reduce the number of packages that were not available by running the following command

```
conda config --append channels conda-forge
```

Bug: Conda vs.Pip Install

If you get errors for a few packages, remove them from the requirements.txt file until you successfully created the conda environment.

```
conda create -n MY_ENVIRONMENT_NAME --file requirements.txt
```

Any packages that didn't get installed during creation of conda environment can be pip installed separately in the newly created conda environment.
for example: 

```
pip install hs-restclient==1.3.5
```

### Reproducible Quote of the Day:

"The product of mental labor - science - always stands far below its value, because the labor-time necessary to reproduce it has no relation at all to the labor-time required for its original production."  Karl Marx


