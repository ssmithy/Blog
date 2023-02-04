---
title: "Automate Microsoft Windows Setup."
date: 2023-02-03
draft: true
---

## How to Automate Windows Configuration after Installation

As a programmer I always like my Windows installation setup in a certain way.

There's lots of software to install and lots of settings and preferences to configure.

One of the marks of a good developer in the Pragmatic Programmer is, if you spilled a coffee on your laptop and had to buy another, (search quote) how quickly could you get your machine back up and running?

This guide aims to solve just that problem.

### Chocolatey

Firstly, big love for Chocolatey - this is a big chunk of the project. After installing chocolatey:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
We can then install 95% of applications using this package manager with:

```
choco install 'Application Name' -y
```

(the -y is to say yes to all question / silent install).

### Settings

After that we'll need to configure various windows related settings:

- Power Settings
- Configure Taskbar and Start menu

And of course the most important, Darkmode

### File and Folders 

I also like to move my User Folders (Desktop, Documents, Source code) to a secondary harddrive.
This allows the applications on the main disk to grow at will

<!-- ## Configure Applications

A lot of applications these days tend to have a cloud storage features for configuration. VS Code for example can store settings on GitHub and not only download them when you first login - but also keeps them synchronised between devices.

Some applications however such as OneDrive backup locations need configuring.

Figure out how to do this AutoHotkey??
 -->



