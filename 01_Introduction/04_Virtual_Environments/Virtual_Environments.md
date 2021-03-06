# Virtual Environments

Virtual environments allow you to control Python versions and package versions independently across projects. 

A Python package is code 
that can be used by multiple independent Python programs. Most analyses will require the use of Python packages
such as pandas or seaborn. Virtual environments allow you to use the most recent version of a package for new projects, 
while maintaining the older versions for old projects. 

Here we will highlight two approaches for creating and maintaining virtual environments: venv and conda.

Skip to the [conda](#conda) section if you 
want the virtual environment manager that will work best in most cases.

## venv

venv can be used for creating virtual environments and is included with every Python installation after 
Python 3.3. To test venv, create a new project folder and change directories (`cd`) to this folder using the Terminal. 
To create a new virtual environment enter:

```shell
yourname@something ~ % python3.8 -m venv my_env
```

**Tip**: if you would like to use Python 2.7, for example, and Python 2.7 is installed then use 
`python2.7` instead of `python3.8`

**Tip:** to create an environment with a different name replace `my_env` with the name of your choice    

Check that there's a new folder called my_env in your project folder. 

```shell
yourname@something ~ % ls
```

Activate the virtual environment

```shell
yourname@something ~ % source my_env/bin/activate
```

You can now use Python in your new virtual environment

```shell
(my_env) yourname@something ~ % python
```

Test Python by entering

```shell
>>>1+1
```

To quit Python enter

```shell
>>>quit()
```

Finally, to deactivate the virtual environment enter

```shell
(my_env) yourname@something ~ % deactivate
```

For more information about how to use venv, see the official documentation 
[here](https://docs.python.org/3/library/venv.html).

## conda

Anaconda comes with a virtual environment manager. After installing Anaconda,
open the Terminal and create a new virtual environment by entering

```shell
yourname@something ~ % conda create --name my_env
```

When prompted answer `y` to confirm the installation location.


**Tip**: if you would like to use a different version of Python, say Python 2.7, enter 
`conda create --name my_env python=2.7`

**Tip:** to create an environment with a different name replace `my_env` with the name of your choice

To activate the virtual environment enter

```shell
yourname@something ~ % conda activate my_env
```

You can now use Python in your new virtual environment

```shell
(my_env) yourname@something ~ % python
```

Test Python by entering

```shell
>>> 1+1
```

To quit Python enter

```shell
>>> quit()
```

Finally, to deactivate the virtual environment enter

```shell
(my_env) yourname@something ~ % conda deactivate
```

For more information about how to use conda to manage virtual environments see the official Anaconda documentation 
[here](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).

## Which Method to Choose?

venv is convenient because it comes pre-installed with Python, so if you do not have Anaconda installed this is the choice
for you. If you do have Anaconda installed, the syntax for using conda is easier to remember 
than venv and thus we recommend conda.

## Creating a virutal environment for computational resources

Now that you know how to make virtual environments, you should make one for this project. 
In the computational-resources directory, create a new virtual environment

```shell
yourname@something ~ % conda create --name comp_resources 
```

And activate the environment 

```shell
yourname@something ~ % conda activate comp_resources
```

Now you can install the Python packages you will need for performing all the analyses
in computational-resources

```shell
(comp_resources) yourname@something ~ pip install -r requirements.txt
```

This command uses the package management software, pip, to install all the packages
specified in the requirements.txt file. A requirements file lists the package names and versions
required for an analysis. Using pip, you
can install any package on the [Python Package Index](https://pypi.org/) (PyPI).

If you are done working with computational-resources for now, you can deactivate the
virtual environment 

```shell
(comp_resources) yourname@something ~ % conda deactivate
```

Every time you are using computational-resources, you should be working in your
comp_resources virtual environment.
