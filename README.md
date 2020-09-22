## :information_source: Required steps after creating a repository from this template :information_source:

### **Create a new project from template**
- Create new project 'NEW-PROJECT'
    - https://github.com/kit-data-manager/template
        - Press green button 'Use this template' in the upper right corner.
    - Configure project
         - Enable this project in coveralls in order to obtain code coverage reports
         - Add branch protection rules in project settings -> branches to require status checks, e.g. Travis Pull and Coveralls, and branches to be up to date for master branch
   
- Fork the project in your local space (YOUR-USERNAME).
- Create a local clone of your fork
    - `git clone https://github.com/YOUR-USERNAME/NEW-PROJECT.git`

- Configure Git to sync your fork with the original NEW-PROJECT repository 
     - `cd NEW-PROJECT`
     - `git remote add upstream https://github.com/kit-data-manager/NEW-PROJECT.git`
- Adapt project to your needs
    - Create branch
        - `git checkout -b firstSettings`
        - Replace all occurences of **template** in this file with your project name 'NEW-PROJECT'
    - Fill in or remove sections of this README.md marked with TODO
    - Remove this section from README.md
    - Commit changes
        - `git add .`
        - `git commit -m "Adapt template for 'NEW-PROJECT'."`
    - Push changes to GitHub
        - `git push -u origin firstSettings`
    - Create pull request on GitHub for branch 'firstSettings'
    - Pull request triggers CI and CodeCoverage. If successful it can be merged to master.
    - Merge pull request in GitHub
    - [Sync fork with upstream repo](https://github.com/kit-data-manager/template/wiki/Manual#Sync-fork-with-upstream-repo)
    - Optional: remove branch to keep your repo clean
        - `git branch -d firstSettings`

Further information will be available
[here](https://github.com/kit-data-manager/template/wiki/Manual).
   
---

# KIT Data Manager - template

![Build Status](https://img.shields.io/travis/kit-data-manager/template.svg)
![Code Coverage](https://img.shields.io/coveralls/github/kit-data-manager/template.svg)
![License](https://img.shields.io/github/license/kit-data-manager/template.svg)

## How to build

In order to build this microservice you'll need:

* OpenJDK 11 or higher

After obtaining the sources change to the folder where the sources are located perform the following steps:

```
user@localhost:/home/user/template$ ./gradlew -Pclean-release build
> Configure project :
Using release profile
<-------------> 0% EXECUTING [0s]
[...]
user@localhost:/home/user/template$
```

The Gradle wrapper will now take care of downloading the configured version of Gradle, checking out all required libraries, build these
libraries and finally build the base-repo microservice itself. As a result, a fat jar containing the entire service is created at 'build/jars/base-repo.jar'.

## How to start

TODO

### Prerequisites

TODO

### Setup

TODO

## More Information

TODO

## License

The KIT Data Manager is licensed under the Apache License, Version 2.0.
