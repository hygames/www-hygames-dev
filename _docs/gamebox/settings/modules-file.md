---
title: The modules file
keywords: gamebox
last_updated: April 22, 2019
tags: [modules, gamebox]
sidebar: gamebox_sidebar
summary: "The modules file contains persistent information about installed modules."
permalink: gamebox/settings/modules-file
folder: settings
---

Example modules file:

```yaml
# This file contains module settings.
# Further documentation can be found at https://www.hygames.co/gamebox/settings/modules-file
# You can modify most of these settings per commands!
# New modules are automatically added to this file when they are installed
# Exemplary module entry (some of these parameters can be optional):
# ------
#  module-id:
#    enabled: true                          If this is false the module will not be loaded
#    autoUpdate: false                      If an update is found, it is automatically installed
#
modules:
  test: 
    - checkForUpdates: true 
      enabled: false
  test-module: 
    - checkForUpdates: true
      enabled: true
```