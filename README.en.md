# VS Code + Git Integration Guide

This document summarizes how to install Git in VS Code, connect with GitHub, and perform basic tasks (commit/push/pull/branch).

## 1) Prerequisites

- Install Git: https://git-scm.com/
- Install VS Code: https://code.visualstudio.com/

## 2) Verify Git installation

If the following command works in PowerShell, installation is complete.

```powershell
git --version
```

## 3) Verify Git detection in VS Code

Open VS Code and check whether Git is detected in the bottom-right or in the Source Control view.
If Git is not found, restart VS Code or verify that the Git install path is on PATH.

Image needed: "Git detected in Source Control view"
![Source Control detected](images/source.png)

## 4) Sign in to GitHub

Sign in to your account in VS Code.

- Open Command Palette: `Ctrl+Shift+P`
- Run "GitHub: Sign in"


## 5) Configure user info

You only need to do this once.

```powershell
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## 6) Connect repository (add remote)

Add a remote repository from a local folder.

```powershell
git init
git remote add origin https://github.com/ubisam-heung/hello-git
git remote -v
```

If a remote already exists, replace it:

```powershell
git remote set-url origin https://github.com/ubisam-heung/hello-git
```

## 7) Basic workflow in VS Code

1. Modify files
2. Check changes in the Source Control view
3. Enter a message and Commit
4. Push or Sync

![commit](images/commit.png)
![push](images/push.png)

## 8) Rename branch to main

```powershell
git branch -m master main
git push -u origin main
```

If master remains on the remote, delete it:

```powershell
git push origin --delete master
```

## 9) Common commands

```powershell
git status
git add .
git commit -m "message"
git push
git pull
```

## 10) Troubleshooting checklist

- Verify Git install: `git --version`
- Restart VS Code
- Verify remote URL: `git remote -v`
- Auth issue: re-login to GitHub in VS Code

---
