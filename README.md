# learning_git_github
Repository created to document the process of learning git and the useful commands i will need in this process
## Install Git
Download Git from this url: https://git-scm.com/downloads  
If you already have Git installed, you can get the latest development version via Git itself:
```
git clone https://github.com/git/git
```
## Setting up Git
### List of commands
Let's put some commands in the terminal (if you are using Windows do not use CMD better use git-bash)
```
git --version 
```
This command will return the version of git we have installed.
```
git config --global user.name "user name"
```
This is to set you username in the global config.
```
git config --global user.email "youremail@yourdomain.com"
```
This is to set your email in the global config.

Once we have set these commands we have configured our git to use this information, the next step will be to configure our code editor, I preferred VScode.  
Download VScode from this url: https://code.visualstudio.com/download  
```
git config --global core.editor "code --wait"
```
This is to set VScode as our default code editor, the "--wait" option is used to make the terminal wait until we close the file we are editing.
```
git config --global -e
```
This command is to open our global configuration file in VScode, if it works the configuration file will open showing us the settings we put before.

