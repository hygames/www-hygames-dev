---
title: Internationalisation
keywords: gamebox
last_updated: June 23, 2019
tags: [modules, gamebox]
summary: "Modules can have there own language files. By default these files should be in a subfolder of the GameBox language directory."
sidebar: gamebox_sidebar
permalink: gamebox/modules/internationalisation
folder: modules
---

By default GameBox provides internationalisation for modules using `yml` files. Strings and String lists are supported. The default implementation [ModuleLanguage] can be used to simplify the process. 

## Using ModuleLanguage

In the Language implementation for modules, [ModuleLanguage], the language files included in the jar are automatically copied into the corresponding language directory. Messages and message lists can be obtained by calling `getMessage(String key)` and `getMessageList(String key)` respectively.

Files can be automatically loaded from either the language directory of the module or from within its jar. A best practise would be to first load a file from the jar containing a complete set of messages as a default language. Then load a file from the language directory (optimally the name of the file should be configurable). This has the upside of guaranteeing no missing messages after an update, since the files in the jar will always be up to date. At the same time all messages contained in later loaded files overwrite the defaults, which results in fully customisable messages.

{% include note.html content='At the moment [ModuleLanguage] loads the "lang_en.yml" file from the jar as a first default language.' %}

An example using Enums to make all messages easily accessible can be seen in the [template module](https://github.com/hygames/gamebox-module-template/blob/master/src/main/java/co/hygames/gamebox/modules/template/TemplateLanguage.java).

[ModuleLanguage]: https://github.com/hygames/gamebox/blob/master/src/main/java/co/hygames/gamebox/language/ModuleLanguage.java
