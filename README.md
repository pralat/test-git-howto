# test-git-howto
# TSSG's Mobile Application Team's Experience with Git & Github

The Mobile Application Development team decided to use git for their project called SleepAnalyzer.
This decision was based on the fact that we felt several job requirements were asking for
experience with git and/or github.

The two big names out there for git repositories are GitHub and Bitbucket. We chose to
use GitHub since it seemed to be synonymous with Git.

## But what is Git
Git is a version control system, think CVS, SCCS, Subversion (SVN), ClearCase, Mercurial, Perforce, etc.

It was written by Linus Torvalds in 2005 to use with the development of the Linux Kernel.
It is now maintained by Junio Hamano.

It is a distributed version control system. This means that the git repository locally on
your machine is a complete repository, with the entire history of all files, and works
independently of network access and independently of other repositories.

## Software
The majority of people in the group use Windows and a few use macOS.

The author has a current prefernce for command line interface vs. GUI.

### GitHub Desktop
Github provides "Github Desktop" for Windows or Mac.

GitHub Desktop download from https://desktop.github.com/

This will install GitHub Desktop and Git Shell.

GitHub Desktop is a GUI driven interface. Some members have run into problems using this.
(TBD Shawn can you remember your issue?)

Git Shell provides a terminal or command window, with a prefered shell with git commands. You set your preference in
the GitHub Desktop settings for the type of shell you want to use:

 + Cmd
 + Git Bash
 + PowerShell
 + Custom


A desktop icon is installed for both GitHub and Git Shell. GitHub can take several "moments" to open (order of minutes sometimes).

The GUI inteface will indicate a download arrow to indicate that there is an update to download.

GitHub has a setting called "Clone Path" that by default is "C:\Users\%USERNAME%\Documents\GitHub"

Git shell will open at this directory as well.

### Git For Windows, macOS, Linux, Solaris

The training some members took for Git suggested in the checklist for preparing for class to install Git from https://git-scm.com/downloads

At this location you could find git downloads for Mac OS X, Windows, Linux and Solaris.

The current (Feb 2017) version of Git for windows is Git-2.11.1-64-bit.exe (Release notes 2017-02-02)

This shell is Mingw64 based - Minimalist GNU for Windows, 64 bit.

It gives quite a nice unix environment. I have been known to open it just to use the shell and unix tools and command line.

## Training
The members of M.A.D. each played around with Git on our own. Some getting further than
others.

One member found training by GitHub and four members decided to take the online training
together.

### Github Training

Offers both instructor led and self-paced online classes.

### Instructor based.
#### GitHub for Developers (6 hours, 2x3hrs over 2 days - instructor led)
The official description says:

Are you a command line user who's new to Git and GitHub? This two-part class will help you learn both — from performing basic Git operations to dealing with merge conflicts in Pull Requests. We'll even rewrite a bit of history, and touch on how to undo (almost) anything with Git.

This is a class for users who are comfortable with a command-line interface.

#### GitHub Essentials (6 hours, 2x3hrs over 2 days - instructor led)
The official description says:

Git on the command line can be easy, and we're here to help! This two-day course will help you master the most commonly used Git operations, starting with core workflows and moving to more advanced Git troubleshooting skills and re-writing history.

This class offers limited exposure to GitHub and is heavy on the command line. If you plan to use GitHub, we recommend GitHub for Developers instead.


Overall, there is a lot of overlap between the two classes, however it was useful to attend both classes.

TBD - expand. Summarize what learned.

GUI clients - there are GUI clients, the instructor mentioned Git Kraken, and Source Tree as popular GUI clients.


#### GitHub Self Paced Training
In addition to the instructor led training GitHub offerts self paced training. I do not know of a M.A.D. member who has taken the online classes.

+ GitHub 101: Introduction to GitHub, ~1hr

+ GitHub 102: Using the GitHub Desktop

+ GitHub 103: Using the Command Line.

+ Git Out of Trouble (Beta)

### GitHub Resources
From the training (aka services) team at GitHub they have a resources section, i.e. https://services.github.com/classnotes/
Official description: "A specially curated list of our favorite resources for learning more about Git and GitHub."

Extra resources cover:
Using Git 
 - book "ProGit v2 by Scott Chacon and Ben Straub, 
 - reference docs,
 - cheat sheets.

Using GitHub 
 - guides,
 - GitHub flow,
 - markdown,
 - fork & pull requests,
 - GitHub Training Youtube Channel https://www.youtube.com/githubguides - Microsoft Virtual Academy: GitHub for Windows

Workflows 
 - GitHub Flow,
 - Git-Flow

Extras
 - Atom - a new open source editor, written by GitHub, tagged "the hackable text editor".
 - Hub is a command-line wrapper for git that makes you better at GitHub.
 
### GitHub Checklists
To prepare you for the class GitHub sends out email with a link to a checklist of items to do
before the class, https://services.github.com/checklists/#developers

The checklist runs through:
1) Create a GitHub account
2) Install Git
3) Check authentication
4) Check your text editor, or install atom
5) Verify you can access gitter

All in all, quite a list to go through to get setup and ready for learning.

## Udacity Training
Another member found a free Udacity course developed by Google:

### How to Use Git and Github
https://www.udacity.com/course/how-to-use-git-and-github--ud775
This starts painfully slow, for non programmers, or for programmers who have never used
version control systems before. It is worth working through it though, since the diagrams
and explanations later on are useful. It is hands on, and you play around in a repository.


### A Beginners Git & GitHub Tutorial
Yet another tutorial http://blog.udacity.com/2015/06/a-beginners-git-github-tutorial.html

Just discovered this one when looking for the URL for the previous class. (Repitition in learning is a good thing).


## Book
The "official" Git book ProGit v2 by Scott Chacon and Ben Straub, https://git-scm.com/book


# So What Do "We" Know Now
During the GitHub classes we used Gitter in order to chat between instructor and students.
Think of slack (don't know SlacK? TV commercial https://www.youtube.com/watch?v=x6sSa5NpqUI )

Gitter is a chat and networking platform that helps to manage, grow and connect communities through messaging, content and discovery.

Gitter and Slack look very similar.

## 1. Configuring git.

Git has 3 levels of configuration: 
1. system wide (--system), for everyone using that machine. Settings saved in $(prefix)/etc/gitconfig
2. global (--global), really for the user. Settings saved in ~/.gitconfig
3. local (--local), for a specific repository. Settings saved in <repo>/.git/config

Typically, after installing git you would want to define your username and email address.

$ git config --global user.name "John Smith"
$ git config --global user.email "john.smith@gmail.com"

### How to handle the age old CRLF issue

$ git config --global core.autocrlf input // if linux or mac

$ git config --global core.autocrlf true // if windows

What editor to use by default for when git wants you to create messages

$ git config --global core.editor {vim, atom, emacs, etc}

$ git config --global push.default simple, matching, upstream

You have the choice of either simple or matching or upstream.
Simple is recommended.
Matching - any local branch will get pushed whenever you do a push

TBD - expand on simple vs matching.

$ git config --list

will display the current configuration.


Locally, when you want to start saving your work in git you would create or move to the working directory.

Using one of the git shells of you choice you would use the command "git init"

"git init" creates a ".git" directory in the working directory, and initializes the directory as a git repository.

The prompt in your command line, will now show (master)

.git is the central "database" for all information related to the git repository.

We can cover the internals of git later on.

If there is an open source project on github that you want to contribute to, or if you want 
to just look at the source code you can take a copy of that repository.

$ git clone <url>

will copy the entire repository specified in the <url> onto your local machine in the current directory.

e.g. 

$ git clone https://github.com/bob01/my-cool-app

bob01 is the name of the user on github, and the repository is "my-cool-app"

You will now have an exact duplicate of the repository, its entire history of changes, and comments.

This is what is meant by a distributed system. Everyone who has a copy, has a complete copy at the time it was taken.


Now you want to make changes
============================
Remember how when you first created a repository with "git init" your prompt changed to include (master).

master is a branch name, and a branch is a pointer. It is a cheap, light weight entity. All that it does is it points to the last commit made.

In 

$ git branch --all

$ git checkout newbutton

$ git remote -v


Two Stage Commit:

working area             staging area           history


$ git add

Adds changes to the staging area

$ git commit

$ git commit -m "Short comment here"

Adds the changes to the history of the repo.


$ git status

$ git log

$ git push


$ git pull

$ git pull --prune

$ git log --oneline

$ git log --oneline --graph

$ git log --oneline --graph --decorate

$ git log --oneline --graph --decorate --all

Phew. Wish there was shorthand for this. ALIAS

$ git alias.s=status

$ git config --global --unset alias.s // removes alias

$ git config --global alias.lol "log --oneline --graph --decorate --all"

and now

$ git lol

is much shorter.



remotes can be anywhere, on the local PC, or on github or bitbucket.

When cloning from a repository, a pull request and branch creation require collaborator status.


Fork is a github concept. It is a clone of the repository on github in to your account on github.
You would then clone the forked copy down onto your local development machine. 

You are then free to create branches, develop and modify your forked copy.

You push changes back to your repository on github. Then to share your changes with the original repo that
you forked you again, issue a pull request. Think of it as you are asking the owner of the repository to review your changes, accept them, and to pull those changes into their repository, hence pull request.

If you are on a team and others have also committed changed to the main repo. how do you get those
changes?

When you clone a repo locally, the origin of the repo is your forked copy. The repo that you forked
from is known as the upstream.

You can request changes from the upstream repo. to be added to your local repo. This can be done 2 ways.
1. You issue a pull command. This command will fetch the changes, add them to your repo. and then merge
the changes in to your working code base.

2a. You issue a fetch command. This will get the changes from the repo. and add them to your repo. This is the first part of the pull command. At this point, you have a record of all the changes made. At this point you can do git status, git diff commands to check and review the changes. 

2b. Then, when you are happy, you can merge the changes in to your local working code base.



## Branches? What are they?


Technically, a branch is a named pointer. By default you get a master branch. Beyond that, you are
free to create branches to track your change
s. Give them simple names, that logically reflect the
changes you want to do. 


Depending on the work flow model you follow, branches can be deleted.

You create new branches with 

$ git branch <new branch name>

then to switch to <new branch name> you use

$ git checkout <new branch name>


A short cut for this is

$ git checkout -b <new branch name>


To see what branches exist just use

$ git branch

without a <new branch name>


Once you have created a pull request, any additional commits to the same branch, will be appended to the
original pull request.


reset and rebase - can be dangerous


## Git Internals
TBD To be continued.


