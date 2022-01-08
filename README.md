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

### :black_nib: Git init <br>

__The command git init creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or to initialize a new,
empty repository. Most other Git commands aren't avaliable outside of an initialized repository, so this is often the first command you run in a new project.__ </br>

```bash 
$ git init
```

__When you use git init by first time inside de git repository, you'll obtain the follow message:__

> __Initialized empty Git repository in C:/Users/macie/OneDrive/Área de Trabalho/teste/.git/__

__When you use the git init command by second time inside the same git repository, you'll obtain the follow message:__

> __Reinitialized existing Git repository in [ directory name ]__ 

<br>

### :gear: Git Config <br>

The command git config is the convenient function used to set Git configuration values in ``--global`` or ``--local`` level projects.
These configuration levels correspond to text files in .gitconfig. Running git config modifies configuration text files.

If you want see the all settings, you can use the follow command:

```bash
$ git config -l
```

> diff.astextplain.textconv=astextplain <br>
> filter.lfs.clean=git-lfs clean -- %f
> filter.lfs.smudge=git-lfs smudge -- %f
> filter.lfs.process=git-lfs filter-process
> filter.lfs.required=true
> http.sslbackend=openssl
> http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt
> core.autocrlf=true
> core.fscache=true
> core.symlinks=false
> pull.rebase=false
> credential.helper=manager-core
> credential.https://dev.azure.com.usehttppath=true
> init.defaultbranch=master
> user.name=Your Name
> user.email=youremail@gmail.com
> core.repositoryformatversion=0
> core.filemode=false
> core.bare=false
> core.logallrefupdates=true
> core.symlinks=false
> core.ignorecase=true
