# Conda

## Why use Conda? 

Conda is another type of virtual environment that you can create as an alternative to using the virtual environments as described in the 03_VirtualEnvironment section of 01_Introduction. The main reason that one would need to use Conda instead of a standard virtual environment is if you want to **specify which version of Python to use**, for standard virtual environments always just use whatever version of Python exists on your laptop. This can occasionally be necessary if you are trying to reproduce code/ a pipeline developed by someone else that uses a version of a package that is not compatible with the most up-to-date version of Python. 

Unlike the standard virtual environment, which is a built-in functionality of Python, you need to download Conda to create a conda virtual environment. 

## Installing Conda

Conda can be installed with homebrew, a package manager that is needed to download some other bioinformatics softwares as well. To install homebrew, open a new Terminal window and enter the following command
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
You *may* need to install x-code first if the above does not work right away (this step takes a while)
```
xcode-select --install
```

Once homebrew is installed, enter the following command in Terminal to use homebrew to install conda. 
```
brew install --cask anaconda
```

Then, run the following command **and restart** Terminal    

```
~/../../opt/homebrew/anaconda3/bin/conda init zsh
```

At this point, you may notice a new part of the stub on your command line that says `(base)`. This signifies that you are in a Conda virtual environment named "base". 
If this is the case, exit the environment by calling
```
(base) yourname@something ~ % conda deactivate
```

Conda will automatically activate into its "base" environment every time you open up a Terminal. To deactivate this behavior, we need to issue the following command
```
conda config --set auto_activate_base false
``` 


## Creating and using a Conda environment 

Once you have conda installed, you can create an environment. The usage below specifies that the conda environment should use Python version 3.8

```
conda create --name my_conda_environment python=3.8
```

Once created, you need to activate your conda environment to use it. You repeat this everytime you open a new terminal to use the virtual environment. 

```
conda activate my_conda_environment
```

If you forget the name of your conda environment, you can use the command ```conda env list``` to see the list of all conda environments that you have created. 

Like with a standard virtual environment, you will know if a conda environment is activated if your line in terminal begins with the name of the environment. 

To install a python package in a conda environment:
```
conda install pip
pip install scikit-learn==0.20.3
```

The command above specifically installed version 0.20.3 of scikit-learn, whereas the command ```pip install scikit-learn``` would default to downloading the most current version of this package. You only need to do ```conda install pip``` upon first making the environment. 

