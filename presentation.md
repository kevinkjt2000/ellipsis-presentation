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

# Demonstration Time



---

# Questions?

