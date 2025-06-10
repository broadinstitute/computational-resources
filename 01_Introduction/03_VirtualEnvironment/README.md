# Virtual Environments 

## Why do we need virtual environments? 

Virtual environments allow you to manage all of your python packages that you use for analysis so that you do not lose them if you perform a software update on your laptop, etc. It also helps to keep all of these packages in one place for instances in which you need to use a version of a package that you do not typically use (i.e. when trying to reproduce code from another lab), in which case you can start a *new* virtual environment to avoid interfering with the packages that are working well for your other projects. 

*Side note*:An alternative to virtual environments as described below are conda environments. We find that these are more complicated than necessary for everyday work. Conda environments allow you to specify which version of Python you want to use, whereas standard virtual environments just use the version of Python that is on your laptop (which is perfectly adequate for everyday/standard analysis). The 04_Additional_Topics folder has a page on Conda if you come across a task that requires using a different version of Python. 

## Create a virtual environment

Create the virtual environment in the home directory of your laptop ("\~") so that it can be accessed regardless of what folder you are in. Call it base_analysis since you will always default to using this virtual environment for any analysis that you do. 

```
python3 -m venv ~/base_analysis
```

*Side note*: NEVER, EVER, EVER create a virtual environment in the Shared Google Drive!! Virtual environments create *many* small files that exhaust the storage on the drive. This is another reason why you should only put virtual environments in your home directory. 

Now that your virtual environment is created, activate it to start using it. 

```
source ~/base_analysis/bin/activate
```

Activating the virtual environment merely makes the packages that are held in it accessible to you, but does not otherwise change how you code/ move around directories etc. You can tell that your virtual environment is activated because the line in Terminal now starts with (base_analysis). 


## Install libraries required for analysis 

The ```pip install``` command adds python packages to the virtual environment that you are in. Install the packages that you need for standard analysis using the requirements.txt file in this GitHub repository.  

```
pip install -r requirements.txt
```

Note that the -r means that you are downloading a list of packages from a file. As you install additional packages to your virtual environment in the future, simply use the command ```pip install packagename```. 


## Exiting and re-entering your virtual environment

Closing the Terminal window will remove you from your virtual environment. You can also manually exit the virtual environment with the command ```deactivate```.

To re-enter your virtual environment (it is good to get into the habit of doing this every time you open Terminal), use the command mentioned previously to activate

```
source ~/base_analysis/bin/activate
```
**TIME-SAVING TIP:** 
Save yourself the energy from typing in Terminal and the brain space for memorizing commands! If you press and hold the ```control``` key and then hit ```R```, you enter "backwards search", in which you can type any part of a command that you have previously used, and Terminal will show the most recent command that includes that term. If the most recent command isn't the one you were looking for, keep hitting ```control  R``` until you get the one you were looking for (or change the search term). If Terminal is showing the command you want to use, simply press enter. If you want to give up on the backwards search, simply hit ```control  C``` ; this is the general command to cancel any task in Terminal (a helpful one to remember for when you accidently do something you did NOT mean to do). 

So for commands that you use often (i.e. activating your virtual environment!!), it's good to get in the habit of just typing ```control + R``` and a short fragment of the command that you know is distinct from other commands you use often (i.e. just start typing out "source" -- this command might even come up as the suggestion as soon as you type s!).

If you don't like using the backwards search feature, the up arrow key always will show you the last command that you used in terminal. So, if you hit that up arrow enough times, you will eventually get back to the last time you activated your virtual environment. This might be the only part of scientific research where it is a good idea to be lazy, so embrace it!  