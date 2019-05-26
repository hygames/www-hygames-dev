---
title: My first Module
keywords: gamebox
last_updated: April 22, 2019
tags: [modules, gamebox]
summary: "You can develop your own module in java and add it to your GameBox installation. If you want to make it available to others you can upload it to the GameBox cloud. "
sidebar: gamebox_sidebar
permalink: gamebox/modules/my-first-module
folder: modules
---

## Prerequisites

Modules are written in Java. For development the GameBox code is needed as a dependency. Using maven, you can add the GameBox repository to your project:
```xml
<project>
    ...
    <repositories>
        ...
        <repository>
            <id>nikls-repo</id>
            <name>Hygames repository</name>
            <url>https://repo.nikl.me/artifactory/public</url>
        </repository>
    </repositories>

    <dependencies>
        ...
        <dependency>
            <groupId>co.hygames</groupId>
            <artifactId>gamebox</artifactId>
            <version>0.0.1</version>
            <scope>provided</scope>
        </dependency>
    </dependencies>
</project>
```

A module's entry point is a class extending ```co.hygames.gamebox.module.GameBoxModule```. This is the only class that is mandatory for a module.

{% include important.html content="Your module needs a *module.json* file with at least a unique id and a valid version! GameBox modules have to use [semantic versioning](https://semver.org/){: target='_blank'}." %}

## Starter module

In the future there will be a started module available that can be used to start working on a new module.

## Locally testing your module

Simply drop your `.jar` into the modules folder and reload GameBox.

## Publish to the cloud

**WIP**
