#### _La version française suit._

# Guide to installing git and knitr on your computer

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
##### Mazal tov! Git should now be set up and ready to use!

### 5. Install R packages for workshop
Open R studio and run the following script to install knitr (useful for working with RMarkdown) and emmeans (useful for effect size analysis) packages. If you don't have R Studio, install it first: [https://rstudio.com/products/rstudio/download/](https://rstudio.com/products/rstudio/download/)

```r
install.packages(c('knitr', 'emmeans'), dependencies = TRUE) 

```
We also recommend you install the tidyverse package for ggplot2, dplyr and some other cool packages that we might get into if we have time.

```r
install.packages("tidyverse")
```


### References
_Installing Git_: [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git "Getting Started - Installing Git")  
_Install Git_: [Bitbucket tutorial](https://www.atlassian.com/git/tutorials/install-git "Install Git")  
_Set up Git_: [GitHub](https://help.github.com/en/github/getting-started-with-github/set-up-git "Set up Git")

***

# Guide pour installer git et knitr sur ton ordinateur

### 1. Vérification rapide pour voir si git est déjà installé.

Ouvrir le __Terminal__ (Mac) or l'__Invite de commande__ ou __Git Bash__ (Windows).  
(Si tu as l'application Git Bash, git devrait déjà être installé.)

```shell
git --version

```
Est-ce que le Terminal/l'Invite de commande te dit ```git version X.XX.X.etc.```? Git est installé.  Excellent.  
Sinon, tu dois installer git.


### 2. Installer git.

Sur __Windows__, installe [git pour Windows](https://gitforwindows.org/ "git pour Windows")  
Sur __Mac__, installe la dernière version compatible utilisant le [git-osx-installer](https://sourceforge.net/projects/git-osx-installer/files/ "git-osx-installer")  
Tu peux revérifier que git est installé en réessayant ```git --version```


### 3. Entrer tes identifiants.

Dans le __Terminal__ ou l'__Invite de commande__/__Git Bash__, entre ton nom d'utilisateur:
```shell
git config --global user.name "PRÉNOM NOM_DE_FAMILLE"
```
_Remplace PRÉNOM et NOM_DE_FAMILLE avec les tiens !_  
  
Entre ton adresse courriel:
```shell
git config --global user.email "COURRIEL"
```
  
Tu peux toujours vérifier tes infos avec ```git config --global user.name``` et ```git config --global user.email```


### 4. Crée un compte GitHub.
Vas à [github.com](https://github.com "GitHub") et crée un compte.

#### Mazal tov ! Git devrait être prêt à utiliser !


### 5. Installez les packages R pour workshop
Ouvrez R studio et exécutez le script suivant pour installer les packages knitr (utile pour utiliser RMarkdown) et emmeans (utile pour l'analyse de la taille de l'effet). Si vous n’avez pas R Studio, installez-le d’abord: [https://rstudio.com/products/rstudio/download/](https://rstudio.com/products/rstudio/download/)

```r
install.packages(c('knitr', 'emmeans'), dependencies = TRUE) 

```
Nous vous recommandons également d'installer le paquet tidyverse pour ggplot2, dplyr et quelques autres paquets intéressants dans lesquels nous pourrions entrer si nous en avions le temps.

```r
install.packages("tidyverse")
```


### Références
_Installing Git_: [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git "Getting Started - Installing Git")  
_Install Git_: [Bitbucket tutorial](https://www.atlassian.com/git/tutorials/install-git "Install Git")  
_Set up Git_: [GitHub](https://help.github.com/en/github/getting-started-with-github/set-up-git "Set up Git")
