# Git
Git is version control system to keep the record of your all versions of your project,we can go to code files of any version and it we can put this files to cloud soo we can acess them from anywhere in the world.

### Terminal Basic Commands
- `pwd` - It gives you present working directory

- `cd foldername` - It changes your current working directory.

-`ls` - It shows you the files and folders available in your working directory.

### Git Config Commands

- git config --global user.name "Shiv" 

    => It sets the global user name of the user.

- git config --global user.email "shivkounsalye@gmail.com"

    => It sets the global email for the name of git user.

- git config list

    => it gives the list of user config on the system.

### Git 3 stage Architecture
Git have 3 stage as mentioned below : 
1. Working Directory : 

    Working directory is the folder space in which you are working in your local computer.

2. Staging Area

    Staging area from which the files will be go to your working repository in the next commit.

    Basically you are making ready your files before pushing. 

3. Git repository 

    Your final repository which is stored on the cloud and the files pushed over their will be the final.

### Git status
`git status` - It gives us the staus of the repository.

### How to make Git Repository
`git init` - It initialize the repository and .git folder in your repository and we can use the git commands in it.

### Git add

- `git add --a` - It brings all the files in to the stagin area.

- `git add filename` - It only add this file to staging area. We can add single file to staging area. 

### Git Commit -m
`git commit -m "First Commit"`
 
It creates the snapshot of your files and store it in your .git folder.

### Git log
`git log` - It shows us our all commits in the .git folders basically all the versions of the snapshot.

### How to clone the repository from the web like github or gitbucket

`git clone url` - It clones the github,gitbucket or web repository and pulls out the all the code to your working directory.  



### How to delete the .git folder and git repository from your working directory

1. **Ubuntu** - `rm -rf .git` - It deletes the .git folder means we will loose the all the commits and git repository from our working directory.

2. **Windows** - `rmdir .git` - It deletes the .git folder means we will loose the all the commits and git repository from our working directory.

If repository has some subfolders then `rmdir /s .git`

### Git file status Lifecycle




