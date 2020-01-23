# Introduction to Version Control

Git is one of several version control solutions available to developers. Version control systems allow developers to track changes that make to their solutions. Developers create `repositories` or `repos` for short, and add their source code to them. 

These systems allow the developer to see exactly what changes were made to source code (diff), when, and by whom. Developers can even go back to earlier versions should they new to view older versions or rollback recent changes should the need arise. 

While there are many different version control solutions, Git is presently the most popular and what we will be using in class.

# Git
Git is a distributed version control system for tracking the history of your code. It is called a `distributed` because it supports both `local` (on the developer's machine) as well as `remote` repositories stored on servers out on the internet/network. A popular remote repository service and one that we will use in class is `Github` (more about that later).

# Practice
## Creating a Git Repo Locally
1. Create a directory to store your application's code.
    ```sh
    cd
    mkdir -p workspace/git-intro
    ```
1. `cd` to that directory
1. Type in the `git init` command
1. You now have a local git repository

## Setting the Username and Email for Git
The first time that you commit anything via Github it will require you to specify the user name and the email address associated with your Github account. You can set and save these settings either for *just* the current repository directory you are in or for all repositories you will work on from your machine. The `-global` option is used to specify that the credentials should be used for all repositories. 

If you intend on interacting with other Github repositories using a different Github user account, then set credentials independently, otherwise, the `-global` option should be used so that you aren't repeatedly prompted for this information.

[Setting the User and email for Git](./img/git-config.png)

## Commiting Changes
1. Create an HTML file with `touch index.html`
1. Create a CSS file with `styles.css`

Since git tracks all changes - unless you tell it to ignore some files, which we will cover later - your two new files will be recognized as new, untracked files by git.

Type `git status` to see the status of all files in your new repository.

### git status
The `status` git command will show you any untracked files as well as those that are tracked, but have been modified in some way. Use this command OFTEN to ensure that any and all local changes get committed and ultimately get pushed to your remote repositories.
[Git init and status Command Output](./img/git_status.gif)

### git add
Next, Tell git that you want to start tracking those files with `git add .` command. The period means "add all untracked files from this directory, and any sub-directories". But be careful! Using the `add .` command means you're adding all untracked files. 

Type `git status` again and notice the new messages that you now have 2 new files that are ready to commit.
[Git Status after Additions](./img/git_status_2.png)

### git restore
If you ever accidentally add files to your repository that were not intended, you can use the `reset` command to back out the additions prior to commit by typing `git reset`.

### git commit
When you are done making additions/changes, you must commit your changes for them to be reflected in your repo. 

You can commit individual files by providing a filename or may commit all added changes by specifying no filename. Every commit requires a commit message. It is CRITICALLY IMPORTANT that you provide a useful commit message that sufficiently explains the changes made.

You may specify the commit message on the command line for convenience using the `-m` option. If you omit this option, the default text editor for the current computer will launch so you can type the commit message. In general, always use the `-m` option.

`git commit -m "Updated nested loops in customer shipment history module so that related shipment information is also populated."`

### git diff
Git maintains a log of all changes made to files within a git repository. Github, discussed below, will show a nice color-coded diff (differences) in the browser, however you can always get a simple version of a diff on your local machine.

The `diff` command shows any differences in your local files and the ones committed to your repository. Text removed from your source code is marked in the color red and preceeded by a `-` sign, while additions will show up in green and preceeded by a `+` sign.
[Git Diff](./img/git_diff.png)

### git log
Github allows easy access to all of the commit messages made while commiting additions/changes to source code, however you can access this log information locally as well by using the `log` git command.

`git log`

[Git log Command Output](./img/git_log.png)
# Using Github

## Creating an Account
> ADD AN IMAGE/ANIMATION

## Creating a Github Repository

## Connecting a Local Repository to a Remote Github Repository
> ADD AN IMAGE/ANIMATION

## git push

## git pull

# Additional Information
+ [git - The Simple Guide](http://rogerdudler.github.io/git-guide/)
