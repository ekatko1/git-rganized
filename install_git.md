# Guide to installing git on your computer

### 1. Quick check to see whether git is already installed.

Open __Terminal__ (Mac) or __Command Prompt__ or __Git Bash__ (Windows).  
(Hint: If you have the Git Bash app, git should already be installed.)

```shell
git --version

```
Is Terminal/Command Prompt telling you ```git version X.XX.X.etc.```? Git is installed.  Nice.  
Otherwise, you need to install git.


### 2. Install git.

For __Windows__ users, install [git for Windows](https://gitforwindows.org/ "git for Windows")  
For __Mac__ users, install the latest compatible version using the [git-osx-installer](https://sourceforge.net/projects/git-osx-installer/files/ "git-osx-installer")
You can check that git is installed by retrying ```git --version```


### 3. Enter your credentials

Back in __Terminal__ or __Command Prompt__/__Git Bash__, enter your user name:
```shell
git config --global user.name "FIRST_NAME LAST_NAME"
```
_Replace FIRST_NAME and LAST_NAME with your own!_  
  
Enter your e-mail address:
```shell
git config --global user.email "EMAIL_ADDRESS"
```
  
You can always check your entries with ```git config --global user.name``` and ```git config --global user.email```


### 4. Create a GitHub account.
Go to [github.com](https://github.com "GitHub") and sign up for an account.


### Mazal tov! Git should now be set up and ready to use!


#### References
_Installing Git_: [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git "Getting Started - Installing Git")  
_Install Git_: [Bitbucket tutorial](https://www.atlassian.com/git/tutorials/install-git "Install Git")  
_Set up Git_: [GitHub](https://help.github.com/en/github/getting-started-with-github/set-up-git "Set up Git")
