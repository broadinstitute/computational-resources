# Installing Python

Here we review how to install Python using either [python.org](python.org) or 
[Anaconda](anaconda.com). 

Skip to the [Full Anaconda Installation](#full-anaconda-installation) section if you
want the Python version that will work best in most cases.

## Motivation

MacOS comes with a built-in version of Python, but relying on this as your primary Python installation is 
problematic because the installation is managed by the operating system, so if you upgrade you may 
lose all of your installed packages, and you may prefer a different version of Python that's either more up to date or compatible with 
a specific analysis pipeline.

## Installing from python.org

Visit [python.org/downloads](python.org/downloads), click on the download button, and follow the graphical installation.

<img src="images/download_python.png" alt="Download" width="200"/>

Check the installation succeeded by entering:

```shell
yourname@something ~ % python3.9
```

Updating `pythonX.X` with whichever version of python you installed. 

This will open a new instance of Python where you can write code

```shell
>>> 1 + 1
```

You can exit Python by entering

```shell
>>> quit()
```

Different versions of Python are all available from the same downloads on python.org.

## Installing from Anaconda

### Full Anaconda Installation

Anaconda comes as a bundle of installations including Python, hundreds of Python packages, an integrated development
environment ([IDE](https://en.wikipedia.org/wiki/Integrated_development_environment)), 
and other software for doing data science. This is useful for setting up a near complete 
data science environment in a single installation. 

The biggest drawback of using the full Anaconda installation is that Anaconda uses 3 GB of space on your computer. 
The large size is a result of all of the
packages that come pre-installed with Anaconda. Miniconda (below) does not come with the pre-installed packages 
and thus is smaller if disk space is a concern.

Installation instructions for Anaconda can be found [here](https://docs.anaconda.com/anaconda/install/mac-os/).
Use the graphical installer [here](https://www.anaconda.com/products/individual). Note: it's okay to skip the 
cryptographic hash verification.

### Miniconda Installation

Miniconda is another distribution of Anaconda, that exclusively
comes with Python and a few essential packages, making it a much smaller installation.

To install miniconda visit the [downloads page](https://docs.conda.io/en/latest/miniconda.html) and click the MacOSX 
download link for your version of interest. The link that ends in 'pkg' will download the graphical installer.

### Using Python with Conda

After installing Anaconda or Miniconda, verify the installation by entering 

```shell
yourname@something ~ % conda --version
```

If you're having trouble verifying your installation, Anaconda has a 
[help page](https://docs.anaconda.com/anaconda/user-guide/troubleshooting/). 

You may notice a new part of the stub on your command line that says `(base)`. If you do not 
see this addition restart terminal and enter

```shell
yourname@something ~ % conda activate
```

This will activate your base environment, from which you can use Anaconda's distribution of Python

```shell
(base) yourname@something ~ % python
```

You can now write python code in the terminal

```shell
>>> 1 + 1
```

To exit Python enter

```shell
>>> quit()
```  

To exit the base Anaconda environment enter

```shell
(base) yourname@something ~ % conda deactivate
```

Unlike downloading Python from python.org, Anaconda comes preloaded with different versions of Python which 
you can use in virtual environments. 

## Which Method to Choose?

We have found the virtual environment manager with Conda easier to use than the managers available for distributions
downloaded from python.org. For this reason, if disk space is not an issue we recommend downloading the Full Anaconda
installation.  
