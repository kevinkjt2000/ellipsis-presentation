---
title: Ellipsis all the .files!
author: Kevin Tindall
patat:
  incrementalLists: true
  wrap: true
  theme:
    header: [vividGreen]
...

---

# What does Ellipsis do?

Ellipsis is a package manager for dotfiles.

---

# What are .files? (a.k.a. dotfiles)

Configuration files in a $HOME directory, such as:

> - .bash_profile
> - .gitconfig
> - .p4config
> - .tmux.conf
> - .vimrc

---

# Dependencies

Just 3 programs are required:

- bash
- curl
- git

---

# Installation

```bash
curl -sL ellipsis.sh | sh
export PATH=$HOME/.ellipsis/bin:$PATH
```

. . .

Yes, you read that correctly.
The website also doubles as an installer.

---

# Creating an Ellipsis package

Initialize a new package with

```bash
ellipsis new <package name>
```

. . .

Then, add dotfiles that you want it to manage

```bash
ellipsis add <package name> <dotfile>
```

---

# Why are all these symlinks being created?

This is how Ellipsis and other tools like it manage your dotfiles from another location in memory.

---

# Backing up the package

Ellipsis packages are git repositories, so you will need access to a git server such as GitHub.

After creating a new repository on GitHub you can push your package for the world to see:

```bash
cd $HOME/.ellipsis/packages/<package name>
git remote add origin git@github.com:<username>/dot-<package name>.git
git push -u origin master
```

---

# Installing a previously backed up package

```bash
ellipsis install <username>/<package name> 
```

---

# But, what if I do not like GitHub?

Then just specify the full URL path to your repository during an ellipsis install.

And for doing a backup, follow instructions from your special git server for pushing an already existing git repo.

---

# Customizing your package with hooks

Ellipsis will use ellipsis.sh from your git repo for any custom operations you would like to perform.

These custom operations are just hooks that the rest of Ellipsis will use instead of the normal defaults.

For example, Using the pkg.install hook it is possible to initialize submodules when installing the package.

<http://docs.ellipsis.sh/en/master/hooks/>

---

# Can my package behave differently based on what OS it is installed on?

Yes.

. . .

There is an API call in Ellipsis that allows your ellipsis.sh script to determine the OS.

---

# Demonstration Time



---

# Questions?

