# Installing Homebrew

[Homebrew](https://brew.sh/) is a package manager for MacOS and Linux and is highly recommend as your first installation, as it will simplify subsequent software installations. 
To install, open a new Terminal window and enter the following command
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
You *may* need to install x-code first if the above does not work right away (this step takes a while)
```
xcode-select --install
```

# Installing Conda

MacOS comes with a built-in version of Python, but relying on this as your primary Python installation is problematic because the installation is managed by the operating system, so if you upgrade you may lose all of your installed packages, and you may prefer a different version of Python that's either more up to date or compatible with a specific analysis pipeline. At GPP, we prefer to use Anaconda for Python version management and as a virtual environment. 

Anaconda comes as a bundle of installations including Python, hundreds of Python packages, an integrated development environment ([IDE](https://en.wikipedia.org/wiki/Integrated_development_environment)), and other software for doing data science. This is useful for setting up a near complete data science environment in a single installation. 

## Anaconda Installation
The biggest drawback of using the full Anaconda installation is that Anaconda uses 3 GB of space on your computer. 
The large size is a result of all of the packages that come pre-installed with Anaconda. If disk space is not an issue we recommend downloading the Full Anaconda installation. 

Enter the following command in Terminal
```
brew install --cask anaconda
```
Verify the installation by entering 

```shell
conda --version
```

# Virtual Environment

Create a new virtual environment by entering

```shell
conda create --name my_env
```

When prompted answer `y` to confirm the installation location.


**Tip**: if you would like to use a different version of Python, say Python 2.7, enter 
`conda create --name my_env python=2.7`

**Tip:** to create an environment with a different name replace `my_env` with the name of your choice

To activate the virtual environment enter
```shell
conda activate my_env
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

Every time you are using computational-resources, you should be working in your comp_resources virtual environment.


