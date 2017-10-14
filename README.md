# Laravel Homestead Tutorial
Step-by-step instructions on setting up Homestead in Windows 7

## Introduction

[Homestead](https://laravel.com/docs/homestead) is a Vagrant box people use to develop [Laravel](https://laravel.com) apps.

Here's how you can get Homestead up and running in Windows 7. This is an alternative to the [official instructions](https://laravel.com/docs/homestead#installation-and-setup).

## Prerequisites

1. You're using Windows 7
2. You have [Git](https://git-scm.com/docs/git-clone) installed
3. You have [VirtualBox](https://www.virtualbox.org) and [Vagrant](https://www.vagrantup.com) installed

## Procedure

1. Download and install (i.e. [add](https://www.vagrantup.com/docs/cli/box.html#box-add)) the [Homestead Vagrant box](https://app.vagrantup.com/laravel/boxes/homestead) into Vagrant

    ```
    $ vagrant box add laravel/homestead
    ```
    
    * Then, you can run `$ vagrant box list` to check which version of the box is installed
    
2. Clone the Homestead Git repository

    ```
    $ git clone https://github.com/laravel/homestead.git ./Homestead
    ```
    
    * That instructs Git to create a folder named `Homestead` in the current directory, and to populate that folder with the contents of the cloned repository
    
3. Check out the latest stable version of the Homestead Git repository

    ```
    $ cd Homestead
    $ git checkout vX.Y.Z
    ```
    
    * Replace the `vX.Y.Z` in the command above, with the tag associated with [this release](https://github.com/laravel/homestead/releases/latest) (i.e. the latest release) of the repository (e.g. `$ git checkout v6.3.0`)
    * The official instructions recommend doing that in case the tip of the *master* branch is not stable

4. Generate the Homestead configuration file (and some other files)

    ```
    $ init.bat
    ```
    
    * That instructs Windows to execute the instructions in that Batch script. One of the instructions is to create a Homestead configuration file (i.e. `Homestead.yaml`) in the current folder
    
5. TO BE CONTINUED...

## Versions

I used the following software versions when writing this document:
1. **Windows 7**: 64-bit with Service Pack 1
2. **Vagrant**: 1.9.6
3. **VirtualBox**: 5.1.14
4. **Homestead Vagrant box**: 3.1.0
5. **Homestead Git repository**: 6.3.0
