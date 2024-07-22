
# Git and GitHub Guide

## Table of Contents
1. [Introduction](#introduction)
2. [Installation and Setup](#installation-and-setup)
   - [Installing Git](#installing-git)
   - [Configuring Git](#configuring-git)
3. [Basic Commands](#basic-commands)
   - [Creating a New Repository](#creating-a-new-repository)
   - [Cloning a Repository](#cloning-a-repository)
   - [Basic Operations](#basic-operations)
   - [Checkout the old version file](#checkout-the-old-version-file)
4. [GitHub Operations](#github-operations)
   - [Creating a GitHub Repository](#creating-a-github-repository)
   - [Pushing to GitHub](#pushing-to-github)
   - [Creating a Pull Request](#creating-a-pull-request)
5. [FAQ](#faq)

## Introduction
Git is a distributed version control system, and GitHub is a cloud-based hosting service for Git repositories. This guide will introduce how to use Git and GitHub for version control and code management.

## Installation and Setup

### Installing Git
Please install Git according to your operating system.

**Windows:**
1. Download the Git installer from [Git for Windows](https://gitforwindows.org/)
2. Follow the installation prompts to complete the installation

**MacOS:**
```bash
brew install git
```

**Linux:**
```bash
sudo apt-get install git
```

### Check git version
```bash
git --version
```

### Configuring Git
After installation, open your command line tool and set your username and email address:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Basic Commands

### Creating a New Repository
Create a new Git repository locally:

```bash
mkdir myproject
cd myproject

git init
```

### Cloning a Repository
Clone an existing repository from a remote server, you can find the repository URL on github (in the green button "Code" in the page of the repository):

```bash
git clone https://github.com/<username>/<repository name>.git
```
you don't need to init if you clone repo from Github

### Basic Operations
**Add files to the staging area:**

```bash
git add filename1 filename2
```
or using "." for all the file in the path

**Commit changes:**

```bash
git commit -m "commit message"
```
after committing, you already done, don't forget to pushing to github

**Changing the latest commit**
keep the commit history
```bash
git revert <commit-hash>
```

**Check status:**

```bash
git status
```
tell you all the file in path is tracked or untracked, staged or unstaged

**View history:**

```bash
git log
```
add "--filename" beehind for specific file history
add "--online" behind for simple history

### Checkout the old version file
**View the old version file**
if you just want to see the old version file, without changing the current version


```bash
git checkout <commit-hash>
```

**Work with old version on new branch**

```bash
git checkout -b <new-branch-name> <commit-hash>
```

**Cover the current version**

```bash
git restore --source=<commit-hash> --staged --worktree .
```

## GitHub Operations

### Creating a new GitHub Repository
1. Log in to your GitHub account
2. Click the “+” icon in the top right corner and select “New repository”
3. Fill in the repository name and description, then click “Create repository”

### Pushing to GitHub
Push changes from your local repository to GitHub:

==remember to add and commit the file first, you can check it with "git status"==
use push to upload the file onto Github, with no branch changes
```bash
git push
```

### Creating a Pull Request
1. After cloning and modifying someone else’s repository on GitHub, commit your changes and push to your branch
2. Open the original repository, click “New pull request”
3. Select your branch, add a description, and click “Create pull request”

## FAQ
### How to merge branches?
Switch to the target branch and execute the merge command:

```bash
git checkout main
git merge feature-branch
```

### How to resolve merge conflicts?
When a merge conflict occurs, Git will prompt the conflicting files. Manually edit these files to resolve conflicts, then add and commit the changes:

```bash
git add conflicted-file
git commit -m "resolved merge conflict"
```

For any questions, please refer to the [Git official documentation](https://git-scm.com/doc) or [GitHub Help Center](https://help.github.com).

