# Basics

## Update System

The software in the system is likely to have become update. Let's update the software in our system (note: all the bash commands are meant to be run on the terminal, but you already know that by now).

```bash
sudo apt-get update
sudo apt-get -y upgrade
```

## Install Java and other utilities

Now we'll go ahead and install some packages that we'll need from time to time (more so if we are going to be using Ubuntu as our primary operating system). Please check the licensing laws in your country for the softwares included in the *restricted* packages below before instaling.

```bash
sudo apt-get install -y software-properties-common curl
sudo apt-get install default-jre default-jdk
sudo apt-get install ubuntu-restricted-extras ubuntu-restricted-addons
```

## Java Alternative

**
* Please note that Java was installed in the last section, and don't actually need to go through this section to install Java.
* This is for adventurous students who wish to install the jdk/jre from Oracle (if you don't know what I am talking about, you don't need to do it.
**

```bash
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update

sudo apt-get install oracle-java8-installer
```

If the Oracle version is the only one you have installed, then you have only one Java framework installed i your system. Otherwise, if you have multiple Java frameworks installed in your system, you can choose one of them with the following:

```bash
sudo update-alternatives --config java
sudo update-alternatives --config javac
```

And here is how you can set up your JAVA_HOME

* Note in the install path from (the command above)
        sudo update-alternatives --config java
* Add JAVA_HOME="YOUR_PATH" to /etc/environment
        source /etc/environment
        echo $JAVA_HOME
        
# Setting up Python

* [What is Anaconda?](https://en.wikipedia.org/wiki/Anaconda_%28Python_distribution%29)
* [Here](http://docs.python-guide.org/en/latest/scenarios/scientific/) is an introduction to the scientific computing stack in Python. You may wish to [navigate](http://docs.python-guide.org/en/latest/scenarios/scientific/#anaconda) to the section on Anaconda.

## Installing Anaconda

* Download: https://www.continuum.io/downloads
    
Distribution | Link
------------ | -----
Linux 64-bit: | https://repo.continuum.io/archive/Anaconda3-4.2.0-Linux-x86_64.sh

* Install
```bash
bash Anaconda3-4.2.0-Linux-x86_64.sh
```

## Testing Anaconda Install

* Verifying Anaconda install
```bash
conda --version
```
* Updating Anaconda to current version
```bash
conda update conda
```
* List installed packages
```bash
conda list
```
* Search for a package
```bash
conda search beautifulsoup4
```
* Install packages
```bash
conda install beautifulsoup4
pip install beautifulsoup4
pip install ipython
```
* Remove packages
```bash
conda remove beautifulsoup4
```

## IPython/Jupyter Notebook Basics

* [Get started with IPython](https://www.youtube.com/watch?v=j08Ry-8MOxM) (ignore the sections on installation)
* You should understand the following concepts:
  - Managing Cells
     * Cell Types
     * Moving Cells around
     * Executing and Creating New Cells
  - Handling Notebooks
     * Creating new notebooks (with different kernels)
     * Exporting notebooks to various formats
  - IPython Kernels
  - Keyboard Shortcuts

IPython Homepage: https://ipython.org/

## Just enough Markdown for Jupyter Notebooks

* [What is markdown?](https://help.github.com/articles/markdown-basics/)
* [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/) (used by IPython)

Here are some examples of markdown in action (edit this cell to see the raw text)
* Styling Text
    - *italicised*
    - **bold**
    - ***italicised and bold***
    - **styles _mixed_ together**
* Unordered lists
  - Nested Unordered Lists
  1. Ordered Lists
    1. Nested Lists
    2. More Nesting
      * More nested lists
* Writing Code Blocks
```R
x = 0
x = 2 + 2
hist(rnorm(1000))
```

# Getting started with Git and GitHub

* Signup for an account in https://github.com/ (remember your github username and password)
* [Setup GitHub](https://help.github.com/articles/set-up-git/) (setup your local *git* installation for GitHub)
```bash
git config --global user.name "YourName"
git config --global user.email "YourGitHubEmailId"
```
* Learn the basics of git
  - [Git the simple guide](http://rogerdudler.github.io/git-guide/)
  - [Set up Git in your machine](http://rogerdudler.github.io/git-guide/)
  - [Practise Git](https://try.github.io/levels/1/challenges/1)
  - [Comparing Git Workflows](https://www.atlassian.com/git/tutorials/comparing-workflows/)
* [GitHub Workflow using web-ui](https://help.github.com/articles/create-a-repo/)
* (Optional for Day 1) [Forking Repos](https://help.github.com/articles/fork-a-repo/) and [GitHub Fork Workflow](https://github.com/sevntu-checkstyle/sevntu.checkstyle/wiki/Development-workflow-with-Git:-Fork,-Branching,-Commits,-and-Pull-Request)
* (Optional for Day 1) [Set up SSH authentication](https://help.github.com/articles/generating-ssh-keys/)


# Mastering Ubuntu and the Terminal

### Mastering Ubuntu

* You should understand the basics of terminal-based manipulation of the operating environment:
  - ls, rm, mv, mkdir, cp
  - top
  - sudo
  - Hidden files
  - An understanding of the file structure (including their home directory)
* You should be able to understand the login process and the way environmental variables are set:
  - .profile
  - .bashrc
  - .bash_history
* You should understand how package management works via apt-get (CLI) and synaptic (GUI):
  - Updating package list (apt-get update)
  - Upgrading to new packages (apt-get upgrade)
  - Adding new repositories to apt (and adding secure keys using apt-key)
  - Adding PPAs
  - Finding and installing new softwares
  - Installing software from .deb files (dpkg -i filename.deb) - walk through the process of installing google chrome (not chromium)
* Introduction to basic tools
  - gedit
  - LibreOffice Calc
  - Changing System Settings
  - Change desktop behaviour
  - Create and set up new users
  - System Monitor (and what do the various components mean)

All most all the topics mentioned above (and a little more) can be found in the following links (strongly suggested that you read these end-to-end if the material is new for you):

* Using the terminal - https://help.ubuntu.com/community/UsingTheTerminal
* Commands on the terminal - https://help.ubuntu.com/community/CommandlineHowto
* Apt-Get Howto - https://help.ubuntu.com/community/AptGet/Howto
* (Optional) Deeper into Apt-Get - https://help.ubuntu.com/community/Repositories/CommandLine
