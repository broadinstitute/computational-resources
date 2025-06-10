
# Getting files from the Broad file server 

The Broad file server is a central storage workspace that all Broadies can access (*if on a Broad computer and connected to the Broad Internal wifi or the VPN*). If you are receiving sequencing data or other large files from another group at the Broad, they may deposit the data on the file server for you to access. Follow this guide to retrieve the data! 

## First: handy tips for using Terminal 

### Essential terminal commands
- ```pwd``` (“print working directory”) 
- ```ls``` (“list files”, or “let’s see what’s in this folder”) 
- - ```ls *.fa``` shows every file in the folder with the .fa ending (you can change this to be another file ending, whatever you want!)
-	- ls A549* shows every file in the folder that begins with “A549”
- cd (“change directory”)
- cd insert/filepath/here to move to a folder that is inside the folder you are currently in
- cd .. to move back/out one folder 
- head filename (previews the designated file in the current folder)

### Shortcuts
- To obtain a (potentially long/annoying) filepath for a file you want to work with, locate the file or folder in Finder and drag into terminal
- Hit tab (on your keyboard) to autocomplete a folder or filename if no others in the current folder have the same name 
- Hit the up arrow on your keyboard to see prior commands you’ve typed out in terminal 
- To see a specific prior command you’ve used in terminal, press control + r, type out a string of characters that you know was in the command, and then keep hitting control + r until terminal shows the command you were looking for. Then hit enter to run the command. 
- control + a to move your cursor to the beginning of the line
- control + e to move your cursor to the end of the line 
- control + a + k to clear a whole line 
- control + c to cancel whatever terminal is doing (“the emergency button”) 


### Space characters in terminal

Terminal reads the space character (“ ”) as the end of a command. It therefore does not like spaces in filepaths, yet many of our google drive folders have spaces in the name! If you try to give a filepath with a space, you will likely get a “No such file or directory” error. Solution: add the escape character (“\”) before every space in the filepath. For example, Shared drives/GPP Cloud becomes Shared\ drives/ GPP\ Cloud
The escape character is automatically inserted when you drag a filepath from finder into terminal, which is just another reason to use that handy shortcut so that you don’t have to worry about this :)  


## Using the Broad file server 

If you are using your Broad-issued laptop and are connected to the Broad Internal wifi (or the VPN), you can simply access the server with the following terminal command 

```
ssh login
```

The very first time you do this, it will give you an ominous warning when you hit enter. Just go along with it!

It will then prompt you to enter your Broad password. Be aware that it will not show that you have entered characters so it will feel as though it’s not tracking as you type your password, but it is. 

This will take you to your home directory in the server. To exit the server, simply use the command ```exit```

### Retrieving a file from the server

In this scenario, we assume that someone has provided you with a filepath to retrieve a file from the server. 

First, use the commands as described in the Terminal tips section to navigate to the folder where you would like this data to go. 

Then, use the following command to move the file from the server to this folder. Note that the file will still exist in its original location on the server. Replace "insert_your_broad_login_here" with your Broad email (before the @...). This will prompt you to enter your password before copying the file down. 

```
scp insert_your_broad_login_here@login.broadinstitute.org:paste_filepath_here .
```

The "." at the end is part of the command; it indicates that file should be moved into the current folder in Terminal. 

If you are copying down an **entire folder**, add -r to the command as shown below 

```
scp -r insert_your_broad_login_here@login.broadinstitute.org:paste_folderpath_here
```
