---
layout: post
title: Using virtualenv
bigimg: /img/path.jpg
---

Virtualenv creates a new isolated Python environment for a project, so that all the dependencies of the project are not mixed up together with other projects or even with the system itself. 

In Pycharm the virtualenv can be created for a project by selecting the Project Interpreter in Settings.

The virtualenv folders for each projects are not advised to be put inside the project's folder as git will also include it to be backed up. Instead, the virrtualenv folders should all be placed together in one place, e.g. ~/virtualenv orr ~/.virtualenv for a hidden folder.
