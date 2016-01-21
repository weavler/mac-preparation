# Basic mac setup for development

# The Perfect Mac OS X Setup for Web Development

> Setting up is always the most **painstaking** part of software development. My goal here is to provide a simple step-by-by guide that walks through the perfect web development setup for Mac OS X. 

## Objectives

- Install **XCode** command line tools
- Set up **Homebrew**
- Install and configure **git**
- Install and configure **nvm** & **Node.JS**
- Install **PostgreSQL** & **MongoDB**
- Add on optional software

## Getting started

We will be doing most of the work within the **Terminal**: 

To open the Terminal in your Mac, simply open up the `Finder` by pressing `command` + `spacebar` and type in **Terminal**.

Once, your Terminal is open, you are ready to begin!

## XCode Command Line Tools

The XCode Command Line Tools Package is a small  package that allows you to do command line development in OS X. It consists of two components: `OS X SDK` and `command-line tools` like Clang, which are installed in `/usr/bin`.

In the Terminal, type the following to install:

```bash
$ xcode-select --install
```

**Note**: *The `$` denotes the beginning of an entry in the terminal. You should not type the '$' in.*

### iOS Development

If you plan on going into Native iOS application development down the road, I recommend you download the whole **[XCode](https://developer.apple.com/xcode/)** package from the App Store.

## Homebrew

[Homebrew](http://brew.sh/) is an open-source software package management system that makes the installation of software a breeze on OS X. 

In the Terminal, type the following to install:

```bash
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Brew Doctor

In the Terminal, type:

```bash
$ brew doctor
```

See what the Doctor says. You may need to edit your ~/.bash_profile or make other adjustments.

### Updating Brew

To update packages in the future, simply run:

```bash
$ brew update
$ brew upgrade
```

### Outdated Brew packages

You can also find out which packages are outdated with:

```bash
$ brew outdated
```

Since Homebrew does not uninstall old versions of a formula, you will accumulate them over time. Simply use:

```bash
$ brew cleanup
```

This command will clean everything at once.

## Git

Install git:

```bash
$ brew install git
```

Configure your name:

```bash
$ git config --global user.name "Insert Name"
```

Then, if [Github](https://github.com) account, insert your email below. Otherwise, [sign up](https://github.com/join).

```bash
$ git config --global user.email insertyouremail@whatever.com
```

To cache your credentials, run in the following command in your Terminal:

```bash
$ git config --global credential.helper cache
```

## NodeJS

[nvm](https://github.com/creationix/nvm) is an awesome Node.JS version manager. The best part? It can be installed easily with Homebrew.

**Rule of Thumb:** *If you are running npm with `sudo`, you are doing it wrong.*


To install or update nvm, you can use the [install script][2] using cURL:

    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.30.2/install.sh | bash

or Wget:

    wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.30.2/install.sh | bash

<sub>The script clones the nvm repository to `~/.nvm` and adds the source line to your profile (`~/.bash_profile`, `~/.zshrc` or `~/.profile`).</sub>

You can customize the install source, directory and profile using the `NVM_SOURCE`, `NVM_DIR`, and `PROFILE` variables.
Eg: `curl ... | NVM_DIR="path/to/nvm" bash`

<sub>*NB. The installer can use `git`, `curl`, or `wget` to download `nvm`, whatever is available.*</sub>

To install the latest version of Node.JS (21/01/2016):

```bash
nvm install 5
```

When you have multiple node versions installed, Choose your version of interest

```bash
nvm use 5
```

## PostgreSQL and MongoDB

PostgreSQL is one of the most advance open-source SQL databases in the world (more on that down the road).

MongoDB is a document-oriented (NoSQL) database. It stands for huMONGOus because it's designed for big data.

In your Terminal, run:

```bash
brew install mongodb postgresql
```

We will be exploring both of these databases more in-depth down the road.

## Optionals

### MacDown

Install [MacDown](http://macdown.uranusjr.com/). MacDown allows you to create, read, and edit Markdown files.

### Java

A lot of programs will require [Java](https://support.apple.com/kb/DL1572?locale=en_US). You can download the latest by googling "Java OS X"


### Atom

[Atom](https://atom.io/) is an open-source text-editor created by [Github](https://github.com). You will need a trustworthy text-editor for your journey. Some alternatives are: [Sublime](http://www.sublimetext.com/), [Vim](http://www.vim.org/), or [Visual Studio](https://www.visualstudio.com/downloads/download-visual-studio-vs).


