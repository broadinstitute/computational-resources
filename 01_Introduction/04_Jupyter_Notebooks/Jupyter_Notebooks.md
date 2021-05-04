# Jupyter Notebooks

Jupyter Notebooks are an interactive programming environment where you can weave
together chunks of text and code to perform analyses. Here we demonstrate how to install and
use Jupyter Notebooks.

## Setup

Using the Terminal create a new project directory and Python 3 virtual environment

```shell
yourname@something ~ % mkdir ~/Documents/test_jupyter
yourname@something ~ % cd ~/Documents/test_jupyter
```

After you have created a project folder, create and activate a new virtual environment

```shell
yourname@something test_jupyter % conda create --name test_jupyter_env
yourname@something test_jupyter % conda activate test_jupyter_env
```

## Installing and Running Jupyter Notebooks

You can install Jupyter Notebooks directly or through Jupyter Lab for an extended 
programming environment.

Both installation methods rely on `pip`, the package installer for Python, which 
can install any package on the [Python Package Index](https://pypi.org/) (PyPI).

### Jupyter Notebook

To install Jupyter Notebooks directly use

```shell
(test_jupyter_env) ... % pip install notebook 
```

Before running a Jupyter Notebook, make your virtual environment available as a Notebook kernel. 
Notebook kernels are instances of Python that each notebook runs on.

```shell
(test_jupyter_env) ... % python -m ipykernel install --user --name test_jupyter_env
```

Now you can start a new Jupyter Notebook session with your virtual environment

```shell
(test_jupyter_env) ... % jupyter notebook
```

Create a new notebook with the test_jupyter_env kernel by selecting New and test_jupyter_env under the 
Notebook heading.

<img src="images/new.png" alt="New" width="106"/>

This will generate a new notebook

<img src="images/notebook.png" alt="Notebook" width="500"/>

### Jupyter Lab 

To install Jupyter notebooks through Jupyter Lab use

```shell
(test_jupyter_env) ... % pip install jupyterlab 
```