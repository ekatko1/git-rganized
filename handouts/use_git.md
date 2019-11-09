# Quick and basic example of working with git

Here is the workflow I attempted to demonstrate during the Git Rganized workshop.

### 1. Create a repository on GitHub.

#### i) Log in to [GitHub](https://github.com/login "GitHub login").

#### ii) Create a __new repository__.

Click __New repository__ from the __+__ dropdown menu on the top-right of the welcome screen next to your profile pic.

![](screenshots/github_new_repos_dropdown.png)

Fill in the fields of the __Create a new repository__ page.  

Choose whether you want your repos to be _public_ or _private_ (you can make private repositories public later). I recommend you click __Initialize this repository with a README__ so you won't forget to create a README later.  I also recommend you add a __.gitignore__ for the scripting language that you use. __Add a license__ to allow other people to use your work. When you're done, click the green __Create repository__ button at the bottom of the screen.

![](screenshots/github_create_repos.png)

### 2. Clone your repository to your computer.

Your repository now exists as a _remote_ repository on GitHub (remote = internet repository version that can be made accessible to other people). To be able to work on your repository from your local computer, you need to _clone_ it to a location on your computer. Click on the green __Clone or download__ button, highlight the URL in the box, and _copy_ it.

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
- ```touch FILE.EXTENSION``` creates a file. E.g. I want to create an R script named _import_data_: ``` touch import_data.R```

Note: UNIX commands have help information accessible by adding the argument ```--help``` after the command.
Also note: UNIX commands are case-sensitive.

### 3. Track changes to your repository.

First, you'll need to make changes to your repository. By changes, I mean you can create one or more files and/or edit  files. You can create files directly from the command line (```touch FILE.EXTENSION```) or drag and drop files into the repository folder from someplace else on your computer. You can similarly edit files like you would any other file elsewhere on your computer, i.e. by opening it and making edits in R, MS Office Suite, a text editor, etc.  

Here's an example where I am creating an R script named _import_data_ and storing it in a subdirectory named _scripts_.

![](screenshots/gitbash_touch.png)

And here is the newly created file in its newly created subfolder.

![](screenshots/documents_import_data.png)

If we open the file _data_import.R_, we can see that it's empty (file size of 0 KB).

![](screenshots/r_empty.png)

But we can go ahead and make an edit. In this example, I've added a small comment to show the 1st edit.

![](screenshots/r_edit1.png)

Time to track changes to this file! Open __Terminal__/__Git Bash__/__Command Prompt__, and navigate to your repository (make sure you are cd'ed _INTO_ your repository!).

![](screenshots/git_add_commit.png)

What I've done here is: 1) checked ```git status``` which let me know the version tracking status of files in the repository; 2) added files to the staging area using ```git add MODIFIED_FILE```; 3) committed changes to the files I added to the staging area using ```git commit -m "COMMIT_MESSAGE"```, where the commit message describes the changes I've made.  

Time to push your commit to your _remote_ (GitHub) repository. The command ```git push origin master``` pushed all your commits since your last push on a particular branch you are working on. In this case, you've been working on the _master_ branch. The ```master``` part of the command ```git push origin master``` refers to the branch you are on, whereas ```origin``` refers to the remote GitHub repository.

![](screenshots/git_push.png)

Go to the GitHub page of your repository (Under the __Repositories__ tab on your profile page > Click on the repository name).

![](screenshots/github_commit.png)

Notice that it shows you now have _2 commits_.

![](screenshots/github_commits.png)

Click on the link in _2 commits_. It contains details of your commits (this is version history!), with specific details about file additions/deletions which represent the changes you committed.

![](screenshots/github_commit1.png)

### Keep making changes and tracking them!

You can go back to your local repository to create and modify files. Repeat the ```git add``` and ```git commit -m "COMMIT_MESSAGE"``` workflow to keep a version history of your files. __Local commits are important!__ They snapshot the version of your repository at a given time. So, __commit often__ to give your future self access to incremental versions of your work. You'll get a feel for how often you should ```git push```.

#### Stay tuned: I'll try to write a short guide to working with branches for collaboration in the near future. Thanks for following along, and don't hesitate to reach out: rebecca.garner@mail.concordia.ca
