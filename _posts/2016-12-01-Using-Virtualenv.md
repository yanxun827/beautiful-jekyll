---
layout: post
title: Using virtualenv
bigimg: /img/path.jpg
published: true
---

Virtualenv creates a new isolated Python environment for a project, so that all the dependencies of the project (modules/packages/executables) are not mixed up together with other projects or even with the system itself, as different versions of each dependency may have backwards incompatible APIs, which will definitely complicate matters.

In Pycharm a virtualenv for a project can be created by selecting the Project Interpreter in Settings.

The virtualenv folders should not be placed within the project's folder, as version control (i.e. git) will include it for backup. This would cause unecessary increase in backup size. Because of this and to make it easier to locate virtualenv folderrs forr different prrojects, it is advised that they should all be placed together in one place, e.g. `~/virtualenv` for a visible folder or `~/.virtualenv` for a hidden folder. Then during deployment, the project's dependencies can be generated within the virtualenv of the project. The command is
```
$ pip freeze > requirements.txt
```
This will create a `requirements.txt` file which will show the eact version of each module being used in the project.

To install modules based on the `requirements.txt` file of a project, simply use the command:
```
$ pip install -r requirements.txt
```
