<h1 align = 'center'> Git-GitHub<h1>

- ** Intro to Git**
- ** Installation**
- ** Git Basics**
- ** Committing In Detail**
- ** Branching**
- ** Merging**
- ** Diffing**
- ** Stashing**
- ** Undoing Changes**
- ** Github Intro**
- ** Fetching & Pulling**
- ** Github Odds & Ends**
- ** Collaborative Workflows**
- ** Rebasing**
- ** Interactive Rebasing**
- ** Git Tags**
- ** Git Behind The Scenes**
- ** Reflogs**
- ** Custom Aliases**

## Introduction to GIT?

- Git is world's mostr popular Version Control System(VCS).
- Version Control System(VCS) - Is a software that tracks and manages changes to files over time.

Git is a distributed version control system (VCS) designed to handle everything from small to very large projects with speed and efficiency. It was created by Linus Torvalds in 2005, initially for developing the Linux kernel, but is now the most widely used VCS in software development.

🔧 What is Git Used For?

- Git helps developers:
- Track changes in source code over time.
- Collaborate on code with others.
- Revert to previous versions of files.
- Manage multiple versions (branches) of a project.
- Merge changes made by different developers.
- Track changes across multiple files.
- Compare versions of a project.
- Time Travel back to old versions.
- Revert to a previous version.
- Collaborate and share changes.
- Comnine Changes.

⚙️ Key Features of Git

1. Distributed System
   Every developer's machine acts as a full-fledged repository with complete history and version tracking.

This means you can work offline and later synchronize with a central server (like GitHub, GitLab, Bitbucket).

2. Fast Performance
   Git is optimized for performance:

Fast commits and branches.

Efficient handling of large repositories.

Low overhead for switching branches and merging.

3. Data Integrity
   Every file and commit is checksummed using SHA-1.

Git ensures integrity, so you can be confident nothing has been altered or corrupted.

4. Branching and Merging
   Git encourages branching, allowing multiple parallel versions of a codebase.

Merging is a powerful feature that integrates changes from different branches.

5. Staging Area (Index)
   Git has a unique staging area, where you can prepare and preview changes before committing them.

❗ Common Misconceptions
Git ≠ GitHub: Git is the version control system; GitHub is a platform to host Git repositories.

GIT:
Git is the version control software that runs locally on your machine. you don't need to register for an account. you don't
need the internet to use it. you can use GIT without ever touching the GITHUB.

GITHUB:
GITHUB is a service that hosts GIT repositories on the cloud and makes it easier to collaborate with other people. You do
need to sign up for an account to use GITHUB. It's an online place to share work that is done using GIT.

**Git is (Primarily) a terminal tool:**
GIT was created as command line tool. To use it, we run various git commands in a Unix shell. This is not the most user
friendly experience, but it's at the very core of Git!.

Popular GIT GUI's Include:

- Github Desktop
- Source Tree
- Tower
- GitKraken
- Ungit

**GUI Clients:**

Pros:

- Way lower barrier-of-entry for beginners compared to the command-line.
- Friendlier to use. Can be a much better experience (when it works).
- Some people prefer the visual experience, even those who can use the command-line.

Cons:

- At times, there is lots of "magic" involved. The inner-workings of Git are obfuscated and hidden away with GUI's.
- Often leads to dependance on a particular piece of software.
- When things go seriously wrong, it can be very challenmging to fix without the command-line.
- The interfaces, buttons, and menus vary between different GUI's/

**The Command Line:**

Pros:

- Git is a command-line tool. All the documentation and resources online will refer to the command-line.
- The command-line can be way faster once you get comfortable with it.
- Some of the more advanced Git features are only available on the command-line.
- The commands are always the same, no matter what machine you are on.

Cons:

- Not beginner friendly. At all. Can be difficult to learn and remember the commands at first.
- Even for some practiced users, the command-line interface is just not a good experience, it's really a matter of preference.

**Why GIT Bash?**

- Bash is a command line interface that is widely used by developers. It is the default shell for Linux and Mac. Git was
  designed to run on a Unix-based interface (Like Bash).

- Windows comes with a different default command line interface called Command Prompt that is not Unix-based.

- Fortunately, we have Git bash! Git Bash is a tool that emulates a Bash Experience on a windows machine. And of course
  it comes with Git too.

To Check the GIT verison installed on the sytem use `git --version`

**Configuring Git:**
This is to know who did the work and who is making changes.
We do not need to register for an account or anything, but we will need to provide:

- Our name
- Our Email

If we are using a GUI, it should prompt you for our name and email the first time open the app.

- To configure the name that git will associate with your work, run this command:
  `git config --global user.name "Nagendra"`
- To verify whether you configured username or not use below command:
  ` git config user.name`

- To configure the Email that git will associate with your work, run this command:
  `git config --global user.email "nagendrareddy29029@gmail.com"`
- To verify whether you configured user email or not use below command:
  ` git config user.email`

## Terminal Crash Course:

- `ls` : Short for list, the contents of a folder or current directory.

Note: To open current directory/path in GUI by using command-line:
Mac - `open .`
Windows - `start .`

We can also use ls with any folder name to list out what are all the files present in that folder. to list out use command
`ls Pets'

We can also chain multiple folder name to see files present in that sub folder
`ls Pets/Cats`

- To open folder directly in GUI mode in Mac use `open Pets`

- `pwd` - Print Working Directory, it just print out your current location(Exact location where you are).

- `cd` - Change Directory(Forward)
  To change to particular folder use `cd Pets`
  To auto-complete the folder name by entering partial name when file name is lengthy we can use `Tab`.

- `cd ..` - Change Directory(Backword one level)

- `touch` : To create a new file or multiple files.
  `touch vegetables.txt`
  `touch car.py images.txt`

  To create a file inside any folder use command `touch Pets/Horses/rocky.txt`

`mkdir` - To create new folders or Directory.
`mkdir Plants`
To create two directories/folders with single action use `mkdir fruits vegetables`

Deleting Files & Folders:
To delete / remove files we have to use command `rm`
`rm cars.py`
`rm fruits.txt vegetables.txt`
We use rm to delete files. but with variation of rm we can also remove/delete folders/directories.
`rm -rf Plants` this command recurssively deletes files/directories.

**What is a GIT Repo?**

Repository:
A GIT repo is a workspace which tracks and manages files within a folder.

Anytime we want to use GIT with a project, app, etc we need to create a new git repository. We can have as many repos on
our machine as needed, all with separate histories and contents.

`git log' to see history of a repo.

`git status` gives information on the current status of a git repository and its contents.

It's very useful, but at the moment we don't actually have any repos to check the status of!

`git init` - we can use this command to create a new git repository. Before we can do anything git-related, we must initialize a repo first.

This is something you do once per project. Initialize the repo in the top-level folder containing your project.

Note: Before initializing a repo in any project folder/directory please make sure to check whether that project file is
already initialized with git by using `git status` command.

**Committing:**
Work On Stuff: Make new files, edit files, delete files, etc.
Add Changes: Group specific changes together, in preparation of committing.
Commit: Commit everything that was previously added.

**GIT Adding:**
Working Directory -> git add -> Staging Area -> git commit -> Repository
`git add file1 file2 file3`

**GIT Commit:**
We use the git commit command to actually commit changes form the staging area.

When making a commit, we need to provide a commit message that summarizes the changes and work snapshotted in the commit.
`git commit` Running git commit will commit all staged changes. It also opens up a text editor and prompts you for a commit
message.

`git commit` with -m flag allows us to pass in an inline commit message, rather than launching a text editor.
`git commit -m "My Message"`

`git log` - Retrieve information for us is a log of the commits for a given repository.
Note: To stage all changes at once use command ` git add .`

**Atomic Commits:**
When possible, a commit should encompass a single feature, change, or fix. In other words, try to keep each commit focused on a single thing.

This makes it much easier to undo or rollback changes later on. It also makes your code or project easier to review.
