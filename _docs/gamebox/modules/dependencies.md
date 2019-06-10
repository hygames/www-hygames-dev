---
title: Module dependencies
keywords: gamebox
last_updated: April 22, 2019
tags: [modules, gamebox]
summary: "Modules can depend on specific versions of GameBox or other modules. "
sidebar: gamebox_sidebar
permalink: gamebox/modules/dependencies
folder: modules
---

## Declaration

Module dependencies are declared in its `module.yml` file. A list of dependencies can be given where each entry defines a specific module by its ID and optionally constrains the needed version to some version range. Modules can use the module ID `gamebox` to depend on a specific version of GameBox.

```yaml
dependencies:
  - id: "gamebox"
    versionConstrain: "~> 1.0"
  - id: "some-dependency"
    versionConstrain: "~> 1.0, >= 1.2"
  - id: "specific-version-dependency"
    versionConstrain: "1.5.3"
```
### Module ID

The unique ID of the dependency. This identifier has to be known for every dependency.

### Version constrains

The setting `versionConstrain` can be a list of several constrains that can use one of the following operators:
1. `>` - any version that is an update to the specified one
2. `<` - any version the specified one is an update to
3. `>=` - the specified version or any update of it
4. `<=` - the specified version or any previous one
5. `=`, `" "` - an equal sign (or no operator) asks for the given specific version
6. `~>` - The [Twiddle Wakka](https://thoughtbot.com/blog/rubys-pessimistic-operator){: target="_blank"}


[RubyGems guide on pessimistic version constraint](https://guides.rubygems.org/patterns/#pessimistic-version-constraint){: target="_blank"}