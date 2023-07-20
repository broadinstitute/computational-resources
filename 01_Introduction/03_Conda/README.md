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

Enter the following command in Terminal
```
brew install --cask anaconda
```

If your Mac has an M-series chip, you need to also run the following command **and restart** Terminal    
**Tip** You can check what chip your Mac has by clicking on the Apple logo on the top left corner of your laptop and click on "About This Mac"
```
~/../../opt/homebrew/anaconda3/bin/conda init zsh
```

At this point, you may notice a new part of the stub on your command line that says `(base)`. This signifies that you are in a Conda virtual environment named "base". 
If this is the case, exit the environment by calling
```shell
(base) yourname@something ~ % conda deactivate
```

Conda will automatically activate into its "base" environment every time you open up a Terminal. To deactivate this behavior, we need to issue the following command
```
conda config --set auto_activate_base false
``` 

# Virtual Environment

Create a new virtual environment named "comp_resources" for the rest of the modules with python version 3.8 by entering

```shell
conda create --name comp_resources python=3.8
```

When prompted answer `y` to confirm the installation location.


**Tip**: if you would like to use a different version of Python, say Python 2.7, enter 
`conda create --name comp_resources python=2.7`

**Tip:** to create an environment with a different name replace `comp_resources` with the name of your choice

To activate the virtual environment enter
```shell
conda activate comp_resources
```

You can now use Python in your new virtual environment

```shell
(comp_resources) yourname@something ~ % python
```

Test Python by entering

```shell
>>> 1+1
```

To quit Python enter

```shell
>>> quit()
```

Now you can install the Python packages you will need for performing all the analyses in computational-resources. Make sure you have this repository cloned and that you are `cd`ed into the computational-resources folder.  

```shell
(comp_resources) yourname@something ~ pip install -r requirements.txt
```

This command uses the package management software, pip, to install all the packages
specified in the `requirements.txt` file. A requirements file lists the package names and versions
required for an analysis. Using pip, you
can install any package on the [Python Package Index](https://pypi.org/) (PyPI).

If you are done working with computational-resources for now, you can deactivate the
virtual environment 

```shell
(comp_resources) yourname@something ~ % conda deactivate
```

Every time you are using computational-resources, you should be working in your comp_resources virtual environment.

For more information about how to use conda to manage virtual environments see the official Anaconda [documentation] (https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).



