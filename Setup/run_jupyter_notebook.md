# Instructions for running Jupyter Notebooks

First, you may want to set up a new Python environment for each project (recommended!) in which you are going to install all the packages.\
Conda has this feature built-in, for pip you can install a package which will handle this for you with `pip install virtualenv` (or install using your OS package manager, see https://virtualenv.pypa.io/en/latest/installation.html).s

Note: If you installed pip using your OS package manager you might have to call `pip3` instead of `pip`.\
 You may always call pip from python as a module: `python -m pip` or `python3 -m pip` depending on how the correct binary for Python is called on your system (in an environment `python` is sufficient).

Then, create a new environment with `conda create -n <env_name> python=3.11` (conda) or `python -m virtualenv <path_to_env> --python python3.11` (virtualenv) - note that this needs Python 3.11 installed for pip or installs Python 3.11 in case of conda since this tutorial needs Python 3.11!\
Afterwards activate the environment with `conda activate <env_name>` (conda) or `source <path_to_env>/bin/activate` (pip).

See also here for documentation: https://docs.conda.io/projects/conda/en/latest/commands/create.html (conda) / https://virtualenv.pypa.io/en/latest/cli_interface.html (virtualenv)

For running these Jupyter Notebooks, make sure to install Jupyter Notebook with pip (`pip install notebook`) or with conda (`conda install -c conda-forge notebook`).\
See the Jupyter Notebook documentation at https://jupyter.org/install#jupyter-notebook for more information.

You may then run Jupyter Notebook in the current directory with `jupyter notebook`.
