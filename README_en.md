# learning_git_github
Repository created to document the process of learning git and the useful commands i will need in this process
https://www.youtube.com/watch?v=VdGzPZ31ts8&t=518s
## Table of Contents
1. [Install Git ](#1-install-git)
2. [Setting up Git](#2-setting-up-git)  
2.1 [List of commands](#21-list-of-commands)    
2.1.1 [Carriage Return](#211-carriage-return)  
2.1.2 [Terminal basic commands](#212-terminal-basic-commands)  
2.1.3 [Initializing Repository](#213-working-with-a-repository)  

## 1. Install Git
Download Git from this url: https://git-scm.com/downloads  
If you already have Git installed, you can get the latest development version via Git itself:
```
git clone https://github.com/git/git
```
## 2. Setting up Git
### 2.1 List of commands
Let's put some commands in the terminal (if you are using Windows do not use CMD better use git-bash)
```
git --version 
```
> This command will return the version of git we have installed.
```
git config --global user.name "user name"
```
> This is to set you username in the global config.
```
git config --global user.email "youremail@yourdomain.com"
```
> This is to set your email in the global config.

Once we have set these commands we have configured our git to use this information, the next step will be to configure our code editor, I preferred VScode.  
Download VScode from this url: https://code.visualstudio.com/download  
```
git config --global core.editor "code --wait"
```
> This is to set VScode as our default code editor, the "--wait" option is used to make the terminal wait until we close the file we are editing.
```
git config --global -e
```
> This command is to open our global configuration file in VScode, if it works the configuration file will open showing us the settings we put before.  

#### 2.1.1 Carriage Return:  
Every time you press "enter" on your keyboard, you insert and invisible character called the end of line or carriage return. This is handle differently on different operating systems.  
When you collaborate on projects with Git and Github, Git might produce unexpected results if, for example, you are working on Windows and your collaborator made changes on macOS.  
You can configure git to handle the end-of-line automatically so you can colaborate effectively with people using other operating systems.  

```
git config --global core.autocrlf input
```
> In case you are using macOS or linux you must use "input" to set up autocrlf.
```
git config --global core.autocrlf true
```
> In case you are using Windows you must use "true" to set up autocrlf.

If you want to know what other configuration possibilities git has you can use
```
git config -h
```

#### 2.1.2 Terminal basic commands
```
ls
```
> The "ls" command will return the list of files in the directory you are currently in.
```
ls -a
```
> The "ls -a" command will return the list of files in the directory you are currently in, including hidden files.
```
pwd
```
> The "pwd" command will return the directory you are actually in.
```
cd <directory>
```
> The "cd" command will allow us to move to another directory, for example, imagine we are in /Desktop, and inside we have a directory called Project, so to access Project we have to type "cd Project" now press enter and you will notice if you use the command "pwd" we are in /Desktop/Project.
```
mkdir <directory>
```
> The "mkdir" command will allow us to create a new directory, for example, if we need to create a directory called "workspace", we must type "mkdir workspace" which will create the workspace directory.

#### 2.1.3 Working with a Repository
```
git init
```
> Once we are inside the directory of our project we must type the command "git init" to initialize the git repository.
```
git add
```
> Adding a file to the stage fase.
```
git add .
```
> The "git add ." command is for adding all files in the repository to the stage phase. Try not to use this too much because it will be a mess if you accidentally add a file you don't want to stage. For example, there are files like large binaries or images or things like the venv file, if you use this command it will push all files into the repository.
```
git commit -m "Description of the commit"
```
> Committing the changes from the stage fase
```
git status
```
> The "git status" command will give us the status of the repository

## Commandos sueltos

```
git log
```
> git log es para ver el historial de commits que se han hecho en el repositorio

```
git remote add origin <direccion del repositorio>
```
> git remote add origin es para agregar el repositorio remoto, en este caso el repositorio de github

```
git pull origin <nombre de la rama>
```
> git pull origin es para traer los cambios que se han hecho en el repositorio remoto, en este caso github

```
git push origin <nombre de la rama>
```
> git push origin es para subir los cambios que se han hecho en el repositorio local, en este caso el repositorio de la computadora

```
git branch
```
> git branch es para ver las ramas que existen en el repositorio

```
```

```
git branch <nombre de la rama>
```
> git branch es para crear una nueva rama


```
git checkout -b <nombre de la rama>
```
> git checkout -b es para crear una nueva rama y moverse a ella

```
git switch -c <nombre de la rama>
```
> git switch -c es para crear una nueva rama y moverse a ella

```
git fetch
```
> git fetch es para traer los cambios que se han hecho en el repositorio remoto, en este caso github

```
git stash
```
> git stash es para guardar los cambios que se han hecho en el repositorio local, en este caso el repositorio de la computadora. Se queda en un estado alternativo llamado `stash`, para devolver los cambios del stash ver `git stash pop`

```

```
git stash pop
```
> git stash pop es para traer los cambios temporales que se han guardado con git stash

```