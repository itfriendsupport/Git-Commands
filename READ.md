Git Commands
============

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |
Basic Git Commands
In this section, you will learn the essential Git commands. These basic Git commands are the foundation to learn more advanced commands. 

Here are the nine useful Git commands.

1. git config
Git config command is super helpful. Especially when you are using Git for the first time, or you have a new Git installation. This command will set up your identity - Name and Email address. And this information will be used with every commit.

Usage

$ git config --global user.name "Your name"  

$ git config --global user.email "Your email"



2. git version
As its name implies, it's just to check which version of Git you are using. At the moment, writing this guide, the latest version of Git for Windows is 2.31.1. It was released on 27th March 2021.

Usage  

$ git version



3. git init
This is probably the first command you use to start a new project in Git. This command will create a blank new repository, and then you can store your source code inside this repo.

Usage  

$ git init 

Or you can use the repository name with your git init command.

$ git init <your repository name>


4. git clone
The git clone command will use an existing repository to copy. There is one main difference between the git init and git clone. 

You will use the Git clone when you need to make a copy on an existing repository. The git clone command internally uses the git init command first and then checks out all its contents.

Usage 

git clone <your project URL>



5. git add
The Git add command will add all the new code files or modified files into your repository. This command offers different options to add files and folders. 

Here is the usage of the Git add command.

Usage

$ git add your_file_name (it will add a single file to your staging area)

$ git add * ( this option will add all the modified and new files to the staging area)



6. git commit
This Git command is essential. Your project quality may drop if you will not use this command appropriately. There is another article about how to use Git commands property, and you can read that here.

In simple words, the Git commit will add your changes to your local repository.

Usage 

$ git commit -m “your useful commit message”



7. git status 
This Git command is convenient to see how many files are there which need your attention. You can run this command at any time. 

You can use it in between Git add, and Git commits to see the status.

Usage 

$ git status 



8. git branch
Most of the time, you have multiple branches in your Git repository. In simple terms, the branch is an independent line of code development. 

With the Git branch command, you can manage your branches effectively. There are many different options and switches of the Git branch. 

To make it simple, here I will highlight how you can create and delete a Git branch (in case you need more depth, you can refer to - Git Branching and Merging section of this article).

Usage 

(i) To list all branches:

$ git branch 


(ii) To create a new branch:

$ git branch <branch_name>


(iii) To delete a branch:

$ git branch -d <branch_name>


9. git checkout
This Git command is used to switch between branches. This is one of the powerful git commands and can use used as a swiss knife, 

In simple words, here is the syntax to switch to another branch.

Usage

$ git checkout <branch_name>

Also, you can create and checkout to a branch in a single like, here is the usage for that 

$ git checkout -b <your_new_branch_name>



Intermediate Level Git Commands
After the basic Git commands, it's time to share with you intermediate Git commands; these Git commands are super helpful if you need to collaborate with your team, share your code with others. Also, there are commands like Git log that will help to see the history of previous commits.

10. git remote
Git remote command acts like a border, and If you need to connect with the outside world, you have to use the Git remote command. This command will connect your local repository to the remote. 

Usage 

$ git remote add <shortname> <url>


Example

$ git remote add origin https://dev.azure.com/aCompiler/_git/DemoProject



11. git push
Once you are connected with the remote repository (with the help of the git remote command), it's time to push your changes to that repository.

Usage 

$ git push -u <short_name> <your_branch_name>

Example 

$ git push -u origin feature_branch


You should have origin and upstream set up before you use Git push. And here is the command to set up upstream.

Usage 

$ git push --set-upstream <short_name> <branch_name>

Example 

$ git push --set-upstream origin feature_branch



13. git fetch 
When you need to download other team members' changes, you have to use git fetch. 

This command will download all information for commits, refs, etc., so you can review it before applying those changes in your local repository.

Usage 

$ git fetch 


14. git pull
The Git pull command downloads the content (and not the metadata) and immediately updates your local repository with the latest content. 

Usage 

$ git pull <remote_url>



15. git stash
This Git command temporarily stores your modified files. You can work in stashed with the following Git command. 

Usage 

$ git stash 

And you can view all of your stashes with the following command 

$ git stash list 

And if you need a apply a stash to a branch, simply use apply 

$ git stash apply 



16. git log
With the help of the Git log, you can see all the previous commits with the most recent commit appear first.

Usage 

$ git log 

By default, it will show you all the commits of the currently checked out branch, but you can force it to see all the commits of all the branches with all options. 

$ git log --all



17. git shortlog
The shortlog command shows you a summary from the Git log command. This command is helpful if you are just interested in the short summary. 

This command is helpful to see who worked on what as it group author with their commits.

Usage 

$ git shortlog  

Git Shortlog Results


18. git show
Compared to the Git log, this command git show will show you details about a specific commit.

Usage 

$ git show <your_commit_hash>



19. git rm
Sometimes you need to delete files from your codebase, and in that case, you can use the Git rm command.

It can delete tracked files from the index and the working directory.

Usage 

$ git rm <your_file_name>



20. git merge
Git merge helps you to integrate changes from two branches into a single branch. 

Usage 

$ git merge <branch_name>

This command will merge the <branch_name> into your current selected branch.



Advanced Level Git Commands
And now the time to up one more level. In this section, you will learn the advanced Git commands. These commands will take time and practice.

Once you know the basics of these commands, it will be easy to use them every day.

21. git rebase 
Git rebase similar to the git merge command. It integrates two branches into a single branch with one exception. A git rebase command rewrites the commit history.

You should use the Git rebase command when you have multiple private branches to consolidate into a single branch. And it will make the commit history linear.

Usage 

$ git rebase <base>



22. git bisect 
The Git bisect command helps you to find bad commits. 

Usage

i) To start the git bisect 

$ git bisect start


ii) let git bisect know about a good commit

$ git bisect good a123 


iii) And let git bisect know about a bad commit

$ git bisect bad z123

With Git bisect you can narrow down the broken code within a few minutes.


23. git cherry-pick 
Git cherry-pick is a helpful command. It's a robust command and allows you to pick any commit from any branch and apply it to any other branch.

Usage

$ git cherry-pick <commit-hash>

Git cherry-pick doesn’t modify the history of a repository; instead, it adds to the history.



24. git archive 
Git archive command will combine multiple files into a  single file. It's like a zip utility, so it means you can extract the archive files to get individual files.

Usage 

$ git archive --format zip HEAD > archive-HEAD.zip

It will create a zip archive of the current revision.



25. git pull --rebase
Most of the time, you need to do rebase (and no merge) when you use Git pull.

In that case, you can use the option

Usage

$ git pull --rebase

It will help you to keep the history clean. Also, you can avoid multiple merges.



26. git blame 
If you need to examine the content of any file line by line,  you need to use git blame. It helps you to determine who made the changes to a file.

Usage 

$ git blame <your_file_name>



27. git tag
In Git, tags are helpful, and you can use them to manage the release. You can think of a Git tag like a branch that will not change. It is significantly more important if you are making a public release.

Usage 

$ git tag -a v1.0.0


28. git verify-commit
The git verify-commit command will check the gpg signature. GPG or “GNU Privacy Guard” is the tool used in sign files and contains their signatures.

Usage 

$ git verify-commit <commit>



29. git verify-tag
In the same way, you can confirm a tag.

Usage 

$ git verify-tag <tag>


30. git diff
Most of the time, you need to compare two git files or branches before you commit or push. Here is a handy command to do that. 

Usage

i) to compare the working directory with the local repo:

$ git diff HEAD <filename>

ii) to compare two branches:

$ git diff <source branch> <target branch>



31. git citool
Git citool is a graphics alternative of the Git commit.

Usage

$ git citool



32. git mv
To rename a git file. It will accept two arguments, source and target file name.

Usage

$ git mv <old-file-name> <new-file-name>



33. git clean
You can deal with untracked files by using the Git clean command. You can remove all the untracked files from your working directory by using this command. In case you want to deal with tracked files you need to use the Git reset command.

Usage

$ git clean



34. git help
There are many commands in Git, and if you need more help with any command, you can use git help at any time from the terminal. 

Usage

$ git help <git_command>



35. git whatchanged
This command does the same thing as git log but in a raw form. And it’s in the git because of historical reasons.
  Git Reset
The term reset stands for undoing changes. The git reset command is used to reset the changes. The git reset command has three core forms of invocation. These forms are as follows.

Soft
Mixed
Hard
If we say in terms of Git, then Git is a tool that resets the current state of HEAD to a specified state. It is a sophisticated and versatile tool for undoing changes. It acts as a time machine for Git. You can jump up and forth between the various commits. Each of these reset variations affects specific trees that git uses to handle your file in its content.

Additionally, git reset can operate on whole commits objects or at an individual file level. Each of these reset variations affects specific trees that git uses to handle your file and its contents.

Git Reset
Git uses an index (staging area), HEAD, and working directory for creating and reverting commits. If you have no idea about what is Head, trees, index, then do visit here Git Index and Git Head.


The working directory lets you change the file, and you can stage into the index. The staging area enables you to select what you want to put into your next commit. A commit object is a cryptographically hashed version of the content. It has some Metadata and points which are used to switch on the previous commits.

Let's understand the different uses of the git reset command.

Git Reset Hard
It will first move the Head and update the index with the contents of the commits. It is the most direct, unsafe, and frequently used option. The --hard option changes the Commit History, and ref pointers are updated to the specified commit. Then, the Staging Index and Working Directory need to reset to match that of the specified commit. Any previously pending commits to the Staging Index and the Working Directory gets reset to match Commit Tree. It means any awaiting work will be lost.

Let's understand the --hard option with an example. Suppose I have added a new file to my existing repository. To add a new file to the repository, run the below command:

$ git add <file name>  
To check the status of the repository, run the below command:

$ git status  
To check the status of the Head and previous commits, run the below command:

$ git log  
Consider the below image:

Git Reset
In the above output, I have added a file named newfile2.txt. I have checked the status of the repository. We can see that the current head position yet not changed because I have not committed the changes. Now, I am going to perform the reset --hard option. The git reset hard command will be performed as:
These options can be

--soft
--mixed
--Hard


$ git reset --hard  


Git Reset
As you can see in the above output, the -hard option is operated on the available repository. This option will reset the changes and match the position of the Head before the last changes. It will remove the available changes from the staging area. Consider the below output:

Git Reset
the status of the repository after the hard reset. We can see there is nothing to commit in my repository because all the changes removed by the reset hard option to match the status of the current Head with the previous one. So the file newfile2.txt has been removed from the repository.

There is a safer way to reset the changes with the help of git stash.

Generally, the reset hard mode performs below operations:


It will move the HEAD pointer.
It will update the staging Area with the content that the HEAD is pointing.
It will update the working directory to match the Staging Area.
Git Reset Mixed
A mixed option is a default option of the git reset command. If we would not pass any argument, then the git reset command considered as --mixed as default option. A mixed option updates the ref pointers. The staging area also reset to the state of a specified commit. The undone changes transferred to the working directory. Let's understand it with an example.

Let's create a new file say newfile2.txt. Check the status of the repository. To check the status of the repository, run the below command:

$ git status  
It will display the untracked file from the staging area. Add it to the index. To add a file into stage index, run the git add command as:


$ git add <filename>  
The above command will add the file to the staging index. Consider the below output:

Git Reset
In the above output, I have added a newfile2.txt to my local repository. Now, we will perform the reset mixed command on this repository. It will operate as:

$ git reset --mixed  
Or we can use only git reset command instead of this command.

$ git reset  
The above command will reset the status of the Head, and it will not delete any data from the staging area to match the position of the Head. Consider the below output:

Git Reset
From the above output, we can see that we have reset the position of the Head by performing the git reset -mixed command. Also, we have checked the status of the repository. As we can see that the status of the repository has not been changed by this command. So it is clear that the mixed-mode does not clear any data from the staging area.

Generally, the reset mixed mode performs the below operations:

It will move the HEAD pointer
It will update the Staging Area with the content that the HEAD is pointing to.
It will not update the working directory as git hard mode does. It will only reset the index but not the working tree, then it generates the report of the files which have not been updated.

If -N is specified on the command line, then the statements will be considered as intent-to-add by Git.

Git Reset Head (Git Reset Soft)
The soft option does not touch the index file or working tree at all, but it resets the Head as all options do. When the soft mode runs, the refs pointers updated, and the resets stop there. It will act as git amend command. It is not an authoritative command. Sometimes developers considered it as a waste of time.


Generally, it is used to change the position of the Head. Let's understand how it will change the position of the Head. It will use as:

$ git reset--soft <commit-sha>  
The above command will move the HEAD to the particular commit. Let's understand it with an example.

I have made changes in my file newfile2.txt and commit it. So, the current position of Head is shifted on the latest commit. To check the status of Head, run the below command:

$ git log  
Consider the below output:

Git Reset


$ git reset --soft  2c5a8820091654  
The above command will shift my HEAD to a particular commit. Consider the below output:

Git Reset
As you can see from the above output, the HEAD has been shifted to a particular commit by git reset --soft mode.

Git Reset to Commit
Sometimes we need to reset a particular commit; Git allows us to do so. We can reset to a particular commit. To reset it, git reset command can be used with any option supported by reset command. It will take the default behavior of a particular command and reset the given commit. The syntax for resetting commit is given below:

$ git reset <option> <commit-sha>  

Usage

$ git whatchanged


### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |
