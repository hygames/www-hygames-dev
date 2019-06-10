---
title: The configuration file
keywords: gamebox
last_updated: April 22, 2019
tags: [modules, gamebox]
sidebar: gamebox_sidebar
summary: "The main configuration file of GameBox is `config.yml` and can be found in the data folder. Here, general settings like the used language file or settings regarding the database are set."
permalink: gamebox/settings/config-file
folder: settings
---

Example configuration file:

```yaml
# This is the main configuration file of GameBox
# For documentation beyond the inline comments, see https://hygames.co/gamebox/settings/config-file

# Settings concerning the module cloud
moduleCloud:
  # set this to false to completely disable the cloud
  enabled: true
  # Weather or not to automatically download compatible updates
  # default value for all modules
  #    this setting can be overwritten for selected modules in 'modules.yml'
  defaultAutoUpdates: false

# The language file to load messages from
languageFile: default
```
