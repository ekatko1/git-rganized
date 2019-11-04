# Quick and basic example of working with git

Here is the workflow I attempted to demonstrate during the Git Rganized workshop.

### 1. Create a repository on Git Hub.

#### i) Log in to [GitHub](https://github.com/login "GitHub login").

#### ii) Create a __new repository__.

Click __New repository__ from the __+__ dropdown menu on the top-right of the welcome screen next to your profile pic.

![](screenshots/github_new_repos_dropdown.png)

Fill in the fields of the __Create a new repository__ page.  

Choose whether you want your repos to be _public_ or _private_ (you can make private repositories public later). I recommend you click __Initialize this repository with a README__ so you won't forget to create a README later.  I also recommend you add a __.gitignore__ for the scripting language that you use. __Add a license__ to allow other people to use your work. When you're done, click the green __Create repository__ button at the bottom of the screen.

![](screenshots/github_create_repos.png)

### 2. Clone your repository to your computer.

Your repository now exists as a _remote_ repository on Git Hub. To be able to work on your repository from your local computer, you need to _clone_ it to a location on your computer. Click on the green __Clone or download__ button, highlight the URL in the box, and _copy_ it.

![](screenshots/github_clone_repos.png)

Open __Terminal__ (on Mac) or __Git Bash__ or __Command Prompt__ (on Windows). Navigate to the folder where you want to store your repository. Use the command ```git clone REPOSITORY_URL``` to clone your repository (_paste_ your copied URL instead of ```REPOSITORY_URL```). In this example, I am cloning my plankton_project repository into my Documents folder.

![](screenshots/gitbash_clone.png)

Optional: you can open the folder containing your cloned repository to _see_ that it's there.

![](screenshots/documents_repos.png)

```cd``` into your repository and list all the files it contains.

![](screenshots/gitbash_ls.png)

You'll notice that the repository contains a folder named __.git/__. This __.git__ folder contains the git version tracking information (so never delete the __.git__ folder!)

#### A very short list of useful UNIX commands to help you navigate on the command line.

- ```cd``` changes the directory (directory = folder). ```cd ..``` moves up one directory. ```cd /``` moves up to the root directory.
- ```pwd``` tells you what directory you are currently in.
- ```ls``` lists the files in the current directory.```ls -lah``` (which is ```ls``` with the argument ```-lah```) lists all files including files with extensions starting with "." (e.g. .git or .gitignore).

Note: UNIX commands have help information accessible by adding the argument ```--help``` after the command.
Also note: UNIX commands are case-sensitive.

### 3. Track changes to your repository.


First, you'll need to make 