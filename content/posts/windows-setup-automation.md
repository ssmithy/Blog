---
title: "Automate Microsoft Windows Setup."
date: 2023-02-03
draft: true
---

## How to Automate Windows Configuration after Installation

As programmers, we like our development environments setup in a particular way.

There's lots of software to install and lots of settings and preferences to configure.

One of the marks of a good developer in the [insert book (pragmatic programmer or clean RCM)] is:
> if you spilled a drink on your laptop and had to buy another, (search quote) how quickly could you get your machine back up and running?

This post aims to explore that problem and potential solutions.

I'm a Microsoft Windows user, so this guide will focus there. These ideas and general concepts can be applied to other systems though - i.e. bash script on linux?
PowerShell is a pre-installed and very useful tool on Windows and that's the tool we'll mostly be using.

### Chocolatey

Big love for [Chocolatey.org](https://chocolatey.org/)! This project simplifies a big chunk of the setup process.

Chocolatey is a package manager manager for Windows that allows you to automate the installation of a lot of software packages.

Firstly, we need to install Chocolatey using an Administrator PowerShell:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Installing applications is then a trivial task of calling the `choco install`.

```
choco install 'Application Package Name' -y
```

(The `-y` is to say yes to all question / silent install).

### Settings

After that we'll need to configure various OS related settings

Power Settings

Taskbar

And of course the most important, **Dark Mode**

### File and Folders

I also like to move my User Folders (Desktop, Documents, Source code) to a secondary hard drive.
This allows the applications on the main disk to grow at will

<!-- ## Configure Applications

A lot of applications these days tend to have a cloud storage features for configuration. VS Code for example can store settings on GitHub and not only download them when you first login - but also keeps them synchronised between devices.

Some applications however such as OneDrive backup locations need configuring.

Figure out how to do this AutoHotkey??
 -->