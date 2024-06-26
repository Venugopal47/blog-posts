# What is Git ?

By far, the most widely used modern version control system in the world today is Git. Git is a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel.

A staggering number of software projects rely on Git for version control, including commercial projects as well as open source. Developers who have worked with Git are well represented in the pool of available software development talent and it works well on a wide range of operating systems and IDEs (Integrated Development Environments).

Having a distributed architecture, Git is an example of a DVCS (hence Distributed Version Control System). Rather than have only one single place for the full version history of the software as is common in once-popular version control systems like CVS or Subversion (also known as SVN), in Git, every developer’s working copy of the code is also a repository that can contain the full history of all changes.

In addition to being distributed, Git has been designed with performance, security and flexibility in mind.

# What is Version Control ?

Version control, also known as source control, is the practice of tracking and managing changes to software code. Version control systems are software tools that help software teams manage changes to source code over time. As development environments have accelerated, version control systems help software teams work faster and smarter.

# Why use git for organization ?

Switching from a centralized version control system to Git changes the way your development team creates software. And, if you’re a company that relies on its software for mission-critical applications, altering your development workflow impacts your entire business.

# How to install git

Before using Git, you need to install it on your system. Git is available for all major operating systems.

- **Windows:** Download and install Git from git-scm.com.
- **macOS:** Install Git using Homebrew with brew install git.
- **Linux:** Use your package manager, e.g., sudo apt-get install git for Ubuntu.
  
# Install Verification

Verify the installation was successful by typing git --version:
```
$ git --version
git version 2.9.2
```

# Configuring Git

Configure your Git username and email using the following commands, replacing Emma’s name with your own. These details will be associated with any commits that you create:
```
$ git config --global user.name "Emma Paris"
$ git config --global user.email "eparis@atlassian.com"
```

# Core Concepts of Git

 ## 1. Repository (Repo):
 A Git repository (or repo) is a collection of files and folders associated with a project, along with metadata stored in a .git directory. It tracks changes and stores the entire history of the project.
## 2. Commit:
A commit represents a snapshot of the project at a particular point in time. It captures changes to files and includes a commit message that describes the changes made.
## 3. Branch:
A branch is a parallel version of the repository that allows developers to work on features or fixes independently without affecting the main codebase. Branches are lightweight and can be merged back into the main branch when ready.
## 4. Remote and Remote Tracking Branches:
A remote is a repository hosted on a server (like GitHub, GitLab) where team members can push and pull changes. Remote tracking branches (e.g., origin/main) are local copies of branches from the remote repository, enabling synchronization of changes.

# Main areas in Git

In Git, the different stages generally refer to different states of your files within the Git workflow. The primary stages in Git are:

- **Modified:** This stage refers to files that have been modified since the last commit. Git tracks these changes, but they are not yet staged for commit.
- **Staged:** Files that have been marked to be included in the next commit are in the staged stage. This means you have used git add to move changes from the modified stage to the staging area.
- **Committed:** Once changes are committed using git commit, they become part of the Git repository's history.

# Git Commands

**1. git config**

```
git config --global user.name "[name]"
git config --global user.email "[email address]"
```
This command sets the author name and email address respectively to be used with your commits.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/e5081413-d0a6-4fd2-b708-e67d7f244f2a)

**2. git init**

```
git init [repository name]
```
This command is used to start a new repository.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/cd2a2604-7d89-4294-b890-cef3437cfdf2)

**3. git clone**

```
git clone [url]
```
This command is used to obtain a repository from an existing URL.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/b50ccffe-ee6f-4d12-b688-b559b0c4042d)

**4. git add**

```
git add [file]
```
This command adds a file to the staging area.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/ec64b226-8131-4454-872c-8340425a6a10)
```
git add *
```
This command adds one or more to the staging area.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/959b2a5a-3903-41b5-a18d-0a2f3f7b2579)

**5. git commit**

```
git commit -m “[ Type in the commit message]”
```
This command records or snapshots the file permanently in the version history.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/08aa63c0-de7e-42f6-a67b-11e07b7aea5c)
```
git commit -a
```
This command commits any files you’ve added with the git add command and also commits any files you’ve changed since then.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/f13226d5-e4b7-4000-90e2-7b815719b43f)

**6. git diff**
```
git diff
```
This command shows the file differences which are not yet staged.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/4abc8dfb-054a-468c-87a0-0f077bb20d2e)

```
git diff –staged
```
This command shows the differences between the files in the staging area and the latest version present.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/feb7beb2-9934-4a12-a839-4b06ad25233f)
```
git diff [first branch] [second branch]
```
This command shows the differences between the two branches mentioned.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/8fde65ab-1f41-406d-912d-2d84526d1d9e)

**7. git reset**
```
git reset [file]
```
This command unstages the file, but it preserves the file contents.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/3a5fcceb-5089-4008-8a27-4014f654eb5e)
```
git reset [commit]
```
This command undoes all the commits after the specified commit and preserves the changes locally.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/fc87c14b-37a1-4710-80bd-cc01cb4366b4)
```
git reset –hard [commit] 
`````
This command discards all history and goes back to the specified commit.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/d8d54ab1-a8b6-44b4-a046-76025a07e09d)

**8. git status**
```
git status
```
This command lists all the files that have to be committed.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/99062be5-3f12-4699-90e7-406573c8e28d)

**9. git rm**

```
git rm [file]
```
This command deletes the file from your working directory and stages the deletion.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/0c11939b-7478-4f42-8c2e-e34e486527a9)

**10. git log**

```
git log
```
This command is used to list the version history for the current branch.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/97299ac6-7506-4067-87f0-1f10423f5a32)

```
git log –follow[file]
```
This command lists version history for a file, including the renaming of files also.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/eee27e0d-0741-4c73-b24d-c0cbe04be89e)

**11. git show**

```
git show [commit]
```
This command shows the metadata and content changes of the specified commit.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/e9a7af22-b2f5-4139-b74d-40900b83a488)

**12. git tag**

```
git tag [commitID]
```
This command is used to give tags to the specified commit.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/8bbe9f80-f6ee-4b6e-96ad-b0150ec822b8)

**13. git branch**

```
git branch
```
This command lists all the local branches in the current repository.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/848a187e-bfd6-4df4-a20f-26bc877bad3a)
```
git branch [branch name]
```
This command creates a new branch.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/8a291950-7f02-4e67-b9fe-8fde55d4747b)
```
git branch -d [branch name]
```
This command deletes the feature branch.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/bd1e5e1b-f8b7-4b05-b578-fd6c7b3e1bd1)

**14.git checkout**

```
git checkout [branch name]
```
This command is used to switch from one branch to another.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/b5630c70-427e-43cd-8888-e322fb4c0f9d)
```
git checkout -b [branch name]
```
This command creates a new branch and also switches to it.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/81aafade-f40f-43f3-a08f-75f40e38a821)

**15. git merge**

```
git merge [branch name]
```
This command merges the specified branch’s history into the current branch.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/936cea37-55a2-4694-a13f-cfb093683fde)

**16. git remote**

```
git remote add [variable name] [Remote Server Link]
```
This command is used to connect your local repository to the remote server.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/6170f703-2e3b-4b0e-9abf-2be37fc51036)

**17. git push**

```
git push [variable name] master
```
This command sends the committed changes of master branch to your remote repository.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/60dc8aff-c071-434a-8f84-ff69e5399567)
```
git push [variable name] [branch]
```
This command sends the branch commits to your remote repository.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/e7b7b350-9aff-4a7c-8300-936a7c8c688f)
```
git push –all [variable name]
```
This command pushes all branches to your remote repository.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/2f0bd0e4-1d04-4acd-b15c-778da7c9cf0f)
```
git push [variable name] :[branch name]
```
This command deletes a branch on your remote repository.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/3ef264c2-1be3-4b23-8c04-92ced82e6638)

**18. git pull**

```
git pull [Repository Link]
```
This command fetches and merges changes on the remote server to your working directory.

![image](https://github.com/Venugopal47/blog-posts/assets/97158707/56c74e84-a33a-463f-b20c-998d12ff36e0)

Conclusion

Mastering Git is a critical skill for modern software development, enabling efficient collaboration, version control, and project management. By understanding its core concepts, mastering basic commands, and adhering to best practices, you can leverage Git to manage your projects effectively, enhance productivity, and contribute effectively to collaborative software development.
