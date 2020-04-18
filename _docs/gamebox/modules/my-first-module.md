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

{% include important.html content="Your module needs a *module.yml* file with at least a unique id and a valid version! GameBox modules have to use [semantic versioning](https://semver.org/){: target='_blank'}, as explained further down in [versioning](#versioning)." %}

## Template module

[A template module](https://github.com/hygames/gamebox-module-template){: target='_blank'} is available on GitHub. The code can be used as a basis for any of your own modules.

## Locally testing your module

Simply drop your `.jar` into the modules folder and reload GameBox.

## Versioning

Modules need to follow [semantic versioning](https://semver.org/){: target='_blank'}, as does GameBox. If a module's version is not semantic, it will not load! This is to ensure correct dependency version constrains.

The gist of semantic versioning is as follows:

>Given a version number MAJOR.MINOR.PATCH, increment the:
>
>1. MAJOR version when you make incompatible API changes,
>2. MINOR version when you add functionality in a backwards-compatible manner, and
>3. PATCH version when you make backwards-compatible bug fixes.
>
>Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

Following these rules is especially important for modules that might be used as dependencies for other modules. In this case the author writing the second module will constrain the dependency version to a range of versions based on semantic versioning. For more information on how to declare dependencies for your modules read [Module dependencies]({{ '/gamebox/modules/dependencies' | relative_url }}).

## Publish to the cloud

**WIP**
