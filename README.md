
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
\`\`\`bash
sudo apt-get install git
\`\`\`

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
Clone an existing repository from a remote server:

```bash
git clone https://github.com/username/repository.git
```

### Basic Operations
**Add files to the staging area:**

```bash
git add filename
```

**Commit changes:**

```bash
git commit -m "commit message"
```

**Check status:**

```bash
git status
```

**View history:**

```bash
git log
```

## GitHub Operations

### Creating a GitHub Repository
1. Log in to your GitHub account
2. Click the “+” icon in the top right corner and select “New repository”
3. Fill in the repository name and description, then click “Create repository”

### Pushing to GitHub
Push changes from your local repository to GitHub:

```bash
git remote add origin https://github.com/username/repository.git
git branch -M main
git push -u origin main
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

