# GitHub-Foundations
It is a repo for GitHub Foundations practice. I am going to make a wonderful help doc that can be useful for anyone who wants to learn basic Git commands.

## Git hidden folder
There is a hidden folder in all the repos, called `.git` to indicated that it is a Git project.

To create a git repo in our new project, you can use `git inti` command to initialize the git environment in that repo.

```sh
mkdir /workspaces/temp/new-project
cd /workspaces/temp/new-project
touch README.md
code README.md #Opens the newly created file
git status
git add . #Adds all files in the directory
# Make changes to README.md
git commit -m "README.md is changed"
```

## Git Config
The gitconfig file is what stores your global configuration details for git like Email, Username, Name, and More.
Showing the contents of our `.gitconfig` file 
```sh
git config --list
``` 

When you first configuring the git, you need to give your Name and Email using the following commands:
```sh
git config --global user.name "Your Name" # Sets your name for all Git repositories.
git config --global user.email "your-email@example.com" # This email is used for commits and must match your GitHub/GitLab email for proper attribution.
git config --global core.editor "code --wait" # Sets VS Code as the default Git editor. (For Vim, use "vim" instead of "code --wait".)
git config --global init.defaultBranch main # Ensures new repositories use main instead of master.
```


## Cloning
We can clone a repo in one of the three ways:
1. HTTPS
2. SSH
3. GithubCLI

### HTTPS

In this method, you should get the HTTPS link from the repository for cloning.
Now, got to the terminal and then run the command with the copied HTTPS link:
```sh
git clone https://github.com/veeneedvee/GitHub-Foundations.git
```

### SSH
In this method, you should get the `ssh` link of the repository that you want to clone.
```sh
ssh git@github.com:veeneedvee/GitHub-Foundations.git
```

### GitHub CLI
To clone the repository using GitHub CLI, run the command:
```sh
gh repo clone veeneedvee/GitHub-Foundations
```

## Git Push
To push your changes from a local machine to a remote repo in GitHub, you need to link to that remote repo.

### When not linked
When you are not linked with the remote repo, then you can perform the following steps:

1. Firs, add the remote repo URL:
   
   ```sh
   git remote add origin https://github.com/veeneedvee/GitHub-Foundations.git
   ```

2. Next, push the changes:
   
   ```sh
   git push -u origin main
   ```

### When linked
When you already linked to the remote repo, you can directly push the code changes.

```sh
git push origin main # or `git push origin master` if the main branch is named master
```

### Install and configure GitHub CLI
We can use GitHub CLI to communicate with GitHub service and our local machine.

#### Install GitHub CLI on Mac machines
To install GitHub CLI, run the following Homebrew command:
```
brew install gh
```

You can also download directly from the website and install the package (_.pkg_) file.
* Go to: [GitHub CLI Releases](https://github.com/cli/cli/releases)
* Download the `.pkg` file for macOS and install it.

#### Verify installation

After installation, check if gh is installed by running:
```
gh --version
```

#### Authenticate with GitHub
To connect GitHub CLI with your GitHub account:
```
gh auth login
```

To verify the authentication status, run:
```
gh auth status
```

#### Clone a repo using GitHub CLI
To clone a repo using GitHub CLI, run:
```
gh repo clone <repo-owner>/<repo-name>
```

## Git Branches
To list all the branches in a repo, run:
```sh
git branch
```

To create a new branch named `dev`, run:
```sh
git branch dev
```

To switch to the new branch named `dev`, run:
```sh
git checkout dev
```

To create and checkout to a branch, run:
```sh
git checkout -b [branch-name]
```

To delete a branch, run:
```sh
git branch -d [branch-name]
```

To rename a branch, run:
```sh
git branch -m [old-name] [new-name]
```

A common workflow for developers is to create a branch or a feature, and they need to push their branch upstream to the remote name origin:
```sh
git checkout -b my-new-branch
# ... makes changes to files
git add .
git commit -m "my changes"
git push -u origin my-new-branch
```


After making changes to the files, you can push those changes by running the following command:
```sh
git push -u origin dev
```

## Git Merging

## Git Stash
Sometimes you might need to keep aside your uncommitted changes and work on some other project. In that case, you can use the `git stash` feature to keep the uncommitted changes some where and then bring them back when required.

To stash the uncommitted changes to currently working branch, run:
```sh
git stash
```

You can give a name to it for easy identification from a huge list of stashed items.
```sh
git stash save ChangesREADME
```

To know the list of all stashed items, run:
```sh
git stash list
```

To reapply the most recently stashed changes without removing them from the stash, run:
```sh
git stash apply
```

If you have multiple stashes, you can apply a specific one using its index:
```sh
git stash apply stash@{2}
```

To get back the stashed items back to the terminal, run:
```sh
git stash pop
```

If you have multiple stashes, you can apply and remove a specific stash using:
```sh
git stash pop stash@{2}
```











