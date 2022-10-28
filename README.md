<div align="center">
  <img src="https://github.com/Mateus20Barros/Git/blob/main/assets/git_logo.png" height="290px" width="100%">
</div> <br>

__``This article is a simple way how people use "Git", to control your version codes.``__

### <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="45" height="35" align="center"/> Git Control Version <br>

__Git is a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system 
kernel. A staggering number of software projects rely on Git for version control, including commercial projects as well as open source. Developers who have 
worked with Git are well represented in the pool of available software development talent and it works well on a wide range of operating systems and IDEs 
(Integrated Development Environments).__ 

<br>

### :black_nib: Git init

__The command git init creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or to initialize a new,
empty repository. Most other Git commands aren't avaliable outside of an initialized repository, so this is often the first command you run in a new project.__ </br>

```bash 
$ git init
```

__When you use git init by first time inside de git repository, you'll obtain the follow message:__

> __Initialized empty Git repository in C:/Users/way/Archive/.git/__

__When you use the git init command by second time inside the same git repository, you'll obtain the follow message:__

> __Reinitialized existing Git repository in [ directory name ]__ 

---
<br>

### :gear: Git Config

__The command git config is the convenient function used to set Git configuration values in ``--global`` or ``--local`` level projects.
These configuration levels correspond to text files in .gitconfig. Running git config modifies configuration text files.__ <br>

__If you want see the all settings, you can use the follow command:__

```bash
$ git config -l
```
__The follow is the settings in your computer prompt:__

```bash
 diff.astextplain.textconv=astextplain
 filter.lfs.clean=git-lfs clean -- %f
 filter.lfs.smudge=git-lfs smudge -- %f
 filter.lfs.process=git-lfs filter-process
 filter.lfs.required=true
 http.sslbackend=openssl
 http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
 core.autocrlf=true
 core.fscache=true
 core.symlinks=false
 pull.rebase=false
 credential.helper=manager-core
 credential.https://dev.azure.com.usehttppath=true
 init.defaultbranch=master
 user.name=Your Name
 user.email=youremail@gmail.com
 core.repositoryformatversion=0
 core.filemode=false
 core.bare=false
 core.logallrefupdates=true
 core.symlinks=false
 core.ignorecase=true
```

__There're the ``--global``, ``--local`` and ``--system`` commands for specific settings:__

___:small_orange_diamond: ``--global``___

___The global level setting is user specific, that it's applied to operating system users.
Global configuration values are stored in a file located in the user's home directory.___

```bash
$ git config --global -l
```

___:small_orange_diamond: ``--local``___

___It config writes it locally if there is no configuration option. The local level configuration is applied in the repository of the context 
in which the git config is invoked. The local configuration values are stored in a file which can be found in the repository's .git directory: .git/config___

```bash
$ git config --local -l
```

___:small_orange_diamond: ``--system``___

___System level configuration is applied machine wide. It covers all operating system users and all repositories. The system level 
configuration file is in the file git config located outside the system root path.___

```bash
$ git config --system -l
```

__You can change one specific setting by using the correct level ``--global``, ``--local`` or ``--system``, as below:__

```bash
$ git config --global user.name "Your name"
```

---
<br>

### :bricks: Git Clone

__The git cloneit is a command line utility that is used to select an existing repository and create a clone or copy of the destination repository.
The git clone is mainly used to point to an existing repository and make a clone or copy of this repository in the new directory in another location. 
The original repository can be located on the local file system or on protocols that support access by remote machines. The command git clone copies 
an existing Git repository.__

```bash
$ git clone "repository link"
```

---
<br>

### :heavy_check_mark: Git Status

__The command git status displays the conditions of the working directory and staging area.
It lets you see which changes were unprepared, which were not, and which files are not being monitored by Git.
Status results do not display any information about the history of committed projects.__

```bash
$ git status
```

---
<br>

### :inbox_tray: Git add

__The command git adds a working directory change to the staging area. 
It tells Git that you want to include updates to a specific file in the next commit. 
However, git addit has no real and significant effect on the repository changes aren't written even until you run git commit.
Along with these commands, you'll also need git status to see the status of the active directory and staging area.__

```bash
$ git add
```

__The above code adds just one archive by time, but if you've need to adds all files at once, you can put "." the dot after a the word add, as like below:__

```bash
$ git add .
```

---
<br>

### :package: The Staging area

__The main function of the command git add is to promote pending changes in working directory to the area git staging.
The staging area is one of Git's most unique features and it can take some getting used to if you're coming from an SVN (or even Mercurial) context.
It helps to think of it as a buffer between the working directory and the project's history. 
The staging area is considered one of the "three trees" of Git, along with the working directory and commit history.__

---
<br>

### :zap: Git Commit

__At a high level, Git can be considered a schedule management utility. Commits are the structural units of a Git project schedule. They can be considered 
snapshots or milestones along the timeline of a Git project. They are created with the command git commit to capture the state of a project at that moment.__ <br>

__Git snapshots are always committed to the local repository, very different from SVN, which commits a copy of the work to the central repository. Git doesn't 
force you to interact with the central repository until you're done. Just as the staging area is an intermediary between the working directory and the project 
history, each developer's local repository is an intermediary between their respective contributions and the central repository.__

```bash
$ git commit
```

__A shortcut command that immediately creates a commit with a transmitted commit message. By default, it git commit opens the text editor configured in place and 
requests that a commit message be written. Passing the option -m will by pass the text editor's request in favor of an embedded message.__

```bash
$ git commit -m "commit message"
```

---
<br>

### :herb: Git Branch

__A branch represents an independent line of development. Branches act as an abstraction for the edit/stage/commit process. You can think of them as a way to request 
an entirely new working directory, staging area, and project history. New commits are recorded in history for the current branch, which results in a fork in the project's history.__ <br>

__The command git branch allows you to create, list, rename and delete branches. It does not allow you to switch between branches or gather a forked history again.
For this reason, the command git branchis tightly integrated with the git checkout and commands git merge.__

___:small_orange_diamond: Creating a branch:___

___It's important to understand that branches are just pointers to commits. When you create a branch, all Git has to do is create a new bookmark, it doesn't change 
the repository in any other way.___

```bash
$ git branch "branch name"
```

___:small_orange_diamond: List all branches in your repositor:___

```bash
$ git branch
```

___:small_orange_diamond: Rename the current branch to.___

```bash
$ git branch -m "new name"
```

---
<br>

### :mag: Git Checkout

__The command git checkout allows navigating between branches created by git branch. Checking a branch updates the files in the current directory to match
the version stored in that branch and tells Git to write all new commits to that branch. It's like a way to select which line of development you're working on.__

```bash
$ git checkout
```

___:small_orange_diamond: New branches.___

___The Git checkout works side by side with git branch. The command git branch can be used to create a new branch. When you want to start a new resource, create 
a new branch from the branch main using git branch new_branch.___

```bash
$ git checkout -b "new branch"
```

___:small_orange_diamond: Switching Branches.___

__Switching between branches is a simple operation. The following command will point HEAD to the tip of.__

```bash
$ git checkout "branch name"
```

__Git tracks a history of check operations in the reflog. You can run git reflog to view history.__

---
<br>

### :chains: Git Merge

__This Git merge will combine multiple sequences into a unified commit record. In the most frequent use cases, git merge is used to combine two branches.
The following examples in this document will focus on this branch merge pattern. In these scenarios, git merge takes two commit indicators, usually the 
tips of the branch, and finds a common base commit between them. Once Git finds a common base commit, it creates a new "merge commit" combining the changes 
from each queued merge commit sequence.__

```bash
$ git merge
```

__When you sure that to join the branches, you must to back for main branch and in it run the below code to join branches:__

```bash
$ git merge "branch name"
```

---
<br>

### :bar_chart: Git Log

__The command git log displays committed snapshots. It allows you to list and filter project history and search for specific changes. While it git status allows the working directory and staging area to be inspected, it git log only works with committed history.__

___:small_orange_diamond: Show all commit history using standard formatting.___

```bash
$ git log
```

___:small_orange_diamond: Limit the number of commits using . For example, it git log -n 3 will only display 3 commits___

```bash
$ git log -n <limit>
```

___:small_orange_diamond: Leave each commit on just one line. It is useful to get a high level overview of the project's history.___

```bash
$ git log --oneline
```

___:small_orange_diamond: Show the patch representing each commit. This action shows the complete diff of each commit, the most in-depth view you can have 
of the project's history.___

```bash
$ git log -p
```

___:small_orange_diamond: Use the following command to search the history with more precision.___

```bash
$ git log --graph --decorate --oneline
```

* ___``--graph`` - That flag plots a text-based graph of the commits on the left side of the commit messages.___
* ___``--decorate`` - It option adds the branch names or tags of the displayed commits.___
* ___``--oneline`` - It option displays information about commits in a single line, making it easy to quickly navigate between commits.___

---
<br>

### :currency_exchange: Git Push

__Send the specified branch to, along with all the necessary internal commits and objects, creating a local branch in the target repository.
To keep you from over writing commits, Git doesn't allow committing when it results in a non-fast forward merge into the target repository.__

```bash
$ git push <remote>
```

__The command git pushis most often used to publish local modifications to a central repository. After a local repository has been modified, a push command is 
run to share the modifications with remote team members. if you've made changes to your project, you can send the current file using the following command:__

```bash
$ git push origin <branch name>
```

---
<br>

### :yo_yo: Git Pull

__The command git pull is used to fetch and download content from remote repositories and immediately update the local repository so that the contents are the same.
Merging remote upstream changes into the local repository is common in Git based collaboration workflows.__

```bash
$ git pull <remote>
```

__Use the command above if the github repository has changed or added new features, and you want your project to be the same as the other.__

__:link: You can see [Atlassian](https://www.atlassian.com/git/tutorials) for more informations about that one.__

<div align="right">
    :octocat: Made by Mateus Barros🏆
</div>

---
