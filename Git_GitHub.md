# Git & GitHub

## Introduction:

Unlike in olden days where a single person or a small group of people develops a software Nowadays for a software product thousands of people work at once .(This is called collaboration btw)

*   There are situations where one person requires the previous version of the stable code because the code which he edited previously have some bugs.
*   There are also situations where thousands of people needs to edit a software product at once .we cannot edit on a single copy of code thousands of people are involved right.

So to overcome these above hurdles software developers started to copy a file of the stable code in there system individually and started editing that particular code and deploying it.After deploying the code there will be several versions which will be available for us to maintain these versions and do above things we have **"Version control systems"**.(Eg: SVN,GIT)

  

### How It Works?

The classic example of how git works is a bank account .We all remember creating our first bank account right .We create an account with a minimum balance or no balance and we credit /debit some money to that account and the changes will be reflected in our bank statemet / passbook.

so let us take an example

```plain
initial balance  ---  1000/-
credited                500
debited               1000
credited               1000
----------------------------
total amount          1500
```

Just like how by adding and removing the money we are changing the state of our total amount.Many developers change the initial code base and the result code base will be the sum of all these changes.

```plain
Result = start + sum(all changes)
```

In the above example we can consider initial balance as the initial code base state and after changes we will get the present state of the code base and up on that many developers will again make changes and this repeats on and on.

  

*   Additional Note
    
    Creating a Book is also a best example many authors will write the book each one responsible for different aspects some might focus on first chapter, some focus on examples, some focus on summary etc..., so at the end of the day they compile all these aspects and create a product i.e., a book .
    

### EVOLUTION:

Its been 25 years since the beginning of VCS in IT. Ever since then there are several changes which occured in VCS satisfying the needs of the developers according to the changes which came in world.We have 3 types of VCS systems

  

*   DIff based vcs
    
    In the primitive version of VCS we have "Diff based " [VCS.So](http://VCS.So) in this VCS what happens the changes that are made by the developer to the base code will be saved seperately in different files in portions .
    
    The advantage here will be its hugely space saving since we are only saving the changes we have done.But Disadvantage is whenever we require the previous stable version of the code VCS will take a lot of time redo the changes made to the code base and present it to the developer.After that storage space became cheap and developers started to use Centralised vcs .
    
      
    
*   Centralised vcs
    
    In centralized based vcs what happened is they will create a stable code in the server .The developers will fetch and copy the file(branch) in their systems which needs to be changed within the stable code , make changes to it and then will commit it .But the system the developer is working on should always be connected to internet that means whenever you commit the code it will be saved in the root code & whenever you need dependent files you again need to take the copy of the file from the server. And it takes a lot of maintanance for the central code.
    
    Eg: SVN
    
*   Distributed vcs
    
    In Distributed vcs what happens is we will have the entire file copied in our local system . we will make change to this copy file and commit it. Then whenever the vcs was asked alatest vesion of the code it will give the code which is last commited .So here this method consumes a lot of space .that is why developers are instructed not to save large files or don't make any changes in the library because the entire file of the code will be saved with the changes in the library .
    
    Note:The difference between git and svn is , in svn it takes part or portion of the entire code base but in git we copy the entire code base.
    
    Eg: GIT
    
      
    

### WORKING OF GIT:

  

![](https://t43258848.p.clickup-attachments.com/t43258848/1976d68c-0464-4881-8eba-9e2f94f18d5f/image.png)

  

### GIT & GITHUB:

One must remember git is a version control system and github is a hosting service and github has all the features in git but it provided an additional feature i.e., hosting service .Its free for open source codes & student projects but if you want your code to be secure then you need subscription.

  

  

  

![](https://t43258848.p.clickup-attachments.com/t43258848/b03910b0-3fee-4d51-908e-57cc25ef056c/image.png)

  

### GIT DEEP - DIVE:

  

![](https://t43258848.p.clickup-attachments.com/t43258848/c20c16a0-d7ef-4dd8-93f5-48e83f05379b/image.png)

  

Let us imagine whenever you commit (save) it creates a ball with those changes you have made.This ball consists of some fields

**Commit message :** when a developer made some changes in the code to explain his code's functionality and comments he can use this.since a product could have a lots of files to know which change is made by other developers we use this.

Eg: Added video calling

**Committer:** Who is the one who made commited or made changes .

**Commit date:**What is the commit date .

**Parent commit:** Whenever you are doing changes to the copy file ,the copy file on which you made the changes that will become the parent commit .

  

**Note**:Each and every commit will have its unique hash code i.e.. **commit Id**

  

### Git Branch:

Git Branches are used to do concentrated work to the codebase like adding a new feature,fixing a bug which might take several days so we will create seperate branch and develop the feature with several commits in that branch after feature is fully developed the tester will test the feature and add the branch to the master branch i.e., stable codebase.

  

Branch is nothing but a pointer to the commit.we can have several child commits to a parent commits but we will have single parent commit only to any given child commit.

  

![](https://t43258848.p.clickup-attachments.com/t43258848/8acb92a7-918f-4cee-8b67-1687d7711aac/image.png)

  

  

*   **POWERSHELL Vs COMMAND PROMPT**
    
    On the first look PowerShell is pretty similar to cmd. They are both used to run external programs like ping or copy, and give you way to automate tasks by writing a script/batch file.
    
    But PowerShell is a lot more than that.
    
    First of all it provides a very rich set of commands (calleds cmdlets) that integrate deeply with windows and most of Microsoft products.
    
    Eg:(Cmdlets like Get-Process which lists active processes.)
    
    Another big difference is that the output of this command is not just text, it's collection of objects. This is way superior to outputting just text, because you can easily query any property of the object, like its name or memory consumption. In cmd you'd have to parse the output.
    
    Another great thing about PowerShell is its integration with .NET. You can easily use all the classes defined in .NET to program any functionality cmdlets are missing.
    
    You can also integrate the powershell runtime into .NET applications with ease and consume Output PowerShell obkects directly.
    
    All in all, PowerShell is cmd on steroids that let'a you automate and manage Windows more easily
    

  

![](https://t43258848.p.clickup-attachments.com/t43258848/2ebe4ad9-1d63-44d8-92ca-0e0b5f692f0c/image.png)

In git hub "License" file tell us whether we can use & contribute the repository or not.

Here initial commit means when we created our repository git will initially/ commit it once .

  

![](https://t43258848.p.clickup-attachments.com/t43258848/d7a50a60-1168-4921-9f6f-3003d253adff/image.png)

  

```plain
When you use `git add` to stage changes in Git, the changes you made to the file will be reflected in the local copy of the file on disk, but the changes will only be staged and not yet committed. 

To clarify, when you edit a file and save the changes locally on your disk, those changes are saved to the working directory of your Git repository. If you then use `git add` to stage those changes, the changes are moved from the working directory to the staging area/index, but the local copy of the file on disk still reflects the changes you made.

If you do not move the changes to the staging area using `git add`, the changes will not be included in your next commit, and the local copy of the file on disk will remain unchanged.

Once you have staged your changes using `git add`, you can use `git commit` to permanently save the changes to your repository's history.
LOCAL system file commands
```

  

```plain
----------
git status
git add/rm
git commit (directed to commit message which is mandatory)
git push( we will be asked git username)
git log
git checkout
git branch
----
The `git diff` command is used to compare the differences between different versions of a file or directory in your Git repository. By default, `git diff` shows the difference between the working directory (i.e., your local files on disk) and the staging area (i.e., the files that you have added using `git add`).

When you make changes to a file in your working directory, these changes are not immediately reflected in the staging area until you use `git add` to stage them. Therefore, if you have made changes to a file in your working directory but have not yet staged those changes, there will be differences between the working directory and the staging area.

For example, suppose you made changes to a file in your working directory and then added some of those changes to the staging area using `git add`. The `git diff` command would show you the differences between the changes that were added to the staging area and the remaining changes in the working directory that have not yet been staged.

Conversely, if you have staged changes using `git add` but have not yet committed those changes using `git commit`, there will also be differences between the staging area and the last committed version of the file. The `git diff` command can be used to show the differences between the staging area and the last committed version of the file.

In summary, `git diff` shows the differences between two different versions of a file, which could be the working directory and the staging area, or the staging area and the last committed version of the file.
```

  

```plain
================
REMOTE git cloud commands
================
git push
git fetch #to fetch all the changes that we have done in remote 
git pull(git pull is a combination of git fetch & git merge )#to update the fetched code in our local file system we use git pull
resolving conflicts




```

Shortcuts:

After commiting (git commit) we will be directed to message editor and its mandatory we can use

below code without all that hassle.

```plain
git commit -m "Adding numbers"
```

  

As one can see after creating a new branch while checking for the log we can see that the branches here are like a pointer which points towards the parent commit

![](https://t43258848.p.clickup-attachments.com/t43258848/038069fb-1ab0-452b-8d8a-848699074e3c/image.png)

```plain
To clone a git repositor copy the link of the repository and paste it like below in cmdprompt,powershell 


git clone https://github.com/starl441/git_learning.git
---
Alternative of ls in commandprompt is dir 
-------
Alternative for vim,nano in commandprompt is notepad.
--------


git status README.md   #tells us the status of the file like if it is in read color not staged (local file system) if it is in green color (staged).
===============
git add README.md  #to stage a file


git add . # to stage everything in the folder
============
git reset HEAD README.md # to unstage the staged file
or 
git restore --staged README.md 
=============
git diff #gives us the difference between local file system & staged file.
=======
git log #it gives the previous parent commit and all other previous commits
======
git checkout #to go to other branches
=======
git checkout -b ravi4426  #to create a new branch naming it as  ravi4426
=======
gitk #for visual representation of entire git 
==
git branch #to get currently local branches and to show which branch you are in right nwo
==
git fetch # if in the github orgin code we made changes then those changes balls after commit will be applied on our local working directory but remember its only going to get the changes information not the changes will be applied to the working directory donot updates which means the working directly donot change
Note: Use git status to get the number of changes done on the orgin code and how much you are behind
==
git pull #for the changes done in github use the pull command to update the working directory
its combination of git fetch and git merge
==
git merge "orgin/main" 
==
git commit -a  #to commit all the uncommited no need to move the file to staging index it will move it to staging and commit it in a single command
==


```

Even though repository is public we cannot edit it we can only read it so before pushing the code we need the permission for that .for that we need to login or generate ssh key between these two

  

Sure! Here is an example workflow that includes each step from cloning a repository to committing changes:

  

1\. Clone the repository: This will create a local copy of the remote repository on your computer.

```plain
   git clone https://github.com/example-user/example-repo.git
```

2\. Create a new branch: This creates a new branch called "new-feature" based on the current branch you are on.

```plain
   git branch new-feature
```

3\. Switch to the new branch:This switches your working directory to the new branch.

```plain
   git checkout new-feature
```

4 Make changes to the code: Edit some files in the working directory to make your desired changes.

```plain
nano example-repo.git
```

5.Check status :This checks the status of file like whether the file is moved to staging index or not.

```plain
git status #The git status command is useful for seeing the current state of your Git repository and determining which files you need to commit or stage for commit.
```

6.Check the difference: This checks the difference between the working directory with staging index

```plain
git diff
```

7\. Stage your changes: This stages all of your changes in the working directory. You can also stage individual files by specifying their paths.

```plain
   git add example-repo.git
```

8\. Commit your changes:

This creates a new commit with your staged changes and adds a commit message describing the changes.

```plain
 git commit -m "Add new feature"
```

  

7\. Push your changes to the remote repository: This pushes your local changes to the remote repository on the "new-feature" branch.

```plain
   git push origin new-feature
```

8\. Create a pull request:

Go to the repository on GitHub and create a pull request to merge your "new-feature" branch into the main branch.

```plain
git pull
```

  

9\. Review and merge the pull request:

The repository owner can review your changes and merge the pull request if they are satisfied.

  

10\. Update your local repository:

\`\`\`

git checkout main

git pull

\`\`\`

This switches back to the main branch and pulls down any changes made in the remote repository since you last pulled.

  

This is just one example workflow, and there are many variations depending on your specific use case. However, this should give you a good overview of each step from cloning a repository to committing changes.

generating ssh keys for establishing trustee relationship between devices .