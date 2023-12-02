# Package management | Linux | Ubuntu 20 LTS

`apt-get` is a command-line tool for handling packages on Debian-based Linux systems like Ubuntu. It allows you to install, update, upgrade, and manage software packages.

Here's a breakdown of the common commands and their functionalities:


## Update & Upgrade packages

**Update Package Lists**: 
To update the local package index with the latest changes made in the repositories, use:

```bash
sudo apt-get update
```
This command retrieves the latest package information from the repositories specified in `/etc/apt/sources.list` or files in `/etc/apt/sources.list.d/`.

**Upgrade Installed Packages**: 
To upgrade all installed packages to their latest available versions, use:

```bash
sudo apt-get upgrade
```
This command installs the newest versions of all packages currently installed on the system. It does not remove any packages or install new ones.

**Upgrade System Packages**: 
If you want to upgrade the system itself, including installed packages and dependencies, you can use:

```bash
sudo apt-get dist-upgrade
```
This command performs the same function as `upgrade`, but it also handles dependencies intelligently and can remove/install additional packages if necessary to complete the upgrade.


## Search & Install packages

**Search for Packages**: 
To search for a package by name, use: `apt-cache search search_term`
Replace `search_term` with the keyword you're looking for. This command displays a list of packages related to the search term.

```bash
apt-cache search simple-scan
```


**Install New Packages**: 
To install a new package, use: `sudo apt-get install package_name` 
Replace `package_name` with the name of the package you want to install. You can install multiple packages by separating their names with spaces.

```bash
sudo apt-get install simple-scan
```


## Remove & Clean packages

**Remove Packages**: 
To remove a package (and its configuration files) from your system, use: `sudo apt-get remove package_name`

```bash
sudo apt-get remove simple-scan
```
This command removes the specified package while keeping its configuration files intact in case you reinstall it later. 

**Purge Packages:**
If you want to completely remove the configuration files as well, use `purge` instead of `remove`: `sudo apt-get purge package_name`

```bash
sudo apt-get purge simple-scan
```

**Cleaning up Packages**: 
To remove downloaded package files that are no longer required, use:

```bash
sudo apt-get autoclean
```

This command removes only the package files that can no longer be downloaded and are practically useless.

**Note:**
>Remember to use `sudo` before these commands to execute them with administrative privileges. Additionally, be cautious while using `dist-upgrade` as it can make significant changes to your system, and it's recommended to review the proposed changes before proceeding.

>Managing repositories involves editing the `/etc/apt/sources.list` file or files within `/etc/apt/sources.list.d/`. These files contain a list of repositories from which `apt-get` fetches packages. To add or remove repositories, you edit these files using a text editor like `nano` or `vim`. Always be careful when modifying repository sources as it can impact the stability and security of your system.


## Watch on Youtube

> Watch this tutorial on YouTube: [Package management | Linux | Ubuntu 20 LTS](https://www.youtube.com/watch?v=GWpDScHaioE)

<!-- Add more videos as needed -->


## Subscribe our YouTube Channel

> Our YouTube Channel: [CodeInsidePro](https://www.youtube.com/@CodeInsidePro)



