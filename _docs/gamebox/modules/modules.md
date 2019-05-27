---
title: GameBox Modules
keywords: gamebox
last_updated: April 22, 2019
tags: [modules, gamebox]
summary: "Modules can add functionality to GameBox like for example additional games. They can be installed in-game or manually by downloading a `.jar` file into the `modules` folder."
sidebar: gamebox_sidebar
permalink: gamebox/modules
folder: modules
---

## What are modules?

GameBox modules can be installed to add functionality like for example games. Anyone can write a module and make it available for the public by uploading it on the GameBox cloud.

The currently installed modules can be found in a subfolder inside the `modules` folder. The name of the subfolder is the id of the module and usually closely represents the module name (without spaces and other special characters). For a list of currently installed modules you can check the file `modules.yml` in the `modules` folder.


## The module cloud

The module cloud contains publicly available modules. It makes installation a lot easier via in-game commands or a GUI. In the future everyone will be able to upload their own modules to the cloud.


## Installing modules

Modules can be manually installed or via the [module cloud](#the-module-cloud).

Since there is no vetting of modules from third parties, please be careful and backup your server before installing modules. Try to inform yourself about the function of the module beforehand.


### From the cloud

Installing modules from the cloud can be easily done in-game via commands (`modules install <module-id>`) or from a GUI. The GUI method is preferred, since it can show additional information about each module (like the author, a description and release notes) and does not require you to know the module-id.


### Manually

To manually install a module simply drop the `.jar` file in the `modules` folder and reload GameBox.
