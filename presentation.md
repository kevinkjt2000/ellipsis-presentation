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

# What are .files? (a.k.a. dotfiles)

Configuration files in a $HOME directory, such as:

> - .bash_profile
> - .gitconfig
> - .p4config
> - .tmux.conf
> - .vimrc

---

# What does Ellipsis do?

Ellipsis is a package manager for dotfiles.

---

# Dependencies

Just 3 programs are required:

- bash
- curl
- git

---

# Installation

`curl -sL ellipsis.sh | sh`

. . .

Yes, you read that correctly.
The website also doubles as an installer.

---

# Creating an Ellipsis package

Initialize a new package with

   `ellipsis new <package name>`

Then, add dotfiles that you want it to manage

   `ellipsis add <package name> <dotfile>`

---

# Backing up the package

Ellipsis packages are git repositories, so you will need access to a git server such as GitHub.

After creating a new repository on GitHub you can push your package for the world to see:

```bash
cd $HOME/.ellipsis/packages/<package name>
git remote add origin git@github.com:username/dot-package.git
git push -u origin master
```

---

# Demonstration Time



---

# Questions?

