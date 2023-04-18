# Package Management

## Learning goals

- Learn what a package manager is and why they exist
- Learn the basics of *Ubuntu*'s `apt` package manager (installing, removing, and updating packages)

## Introduction

So far we have been using our *Ubuntu* install with the software it came packaged with. What about getting and using other software that doesn't come included in our *Linux* distribution?

In this chapter, we will be taking a look at *package management*. 

## Package Managers

A **package manager** is a software tool that can be used to install, update,
and manage software (packages) on a system. A **package** is simply a collection
of files and data that make up a piece of software or library.

Package managers also automatically manage *dependencies* for packages, which are other packages required for a package to run.

In *Linux*, package managers are dependent on the distribution you have. While most of them behave in effectively the same manner, the way in which you interact with them and the commands used can vary.

In *Ubuntu*, we use the `apt` (Advanced Packaging Tool) package manager.

## `apt`

In order to use `apt`, you simply need to use the `apt` command in the shell as root.

To update the list of packages on your system and retrieve the latest version for each, you can run the `update` command:

```bash
$ sudo apt update
```

That command on its own doesn't actually upgrade the packages themselves; it only updates the list of available packages and whether there are new versions for currently installed ones.

To actually go through and upgrade each installed package that has a new version, you can use the `upgrade` command:

```bash
$ sudo apt upgrade
```

If you want to install a specific package, you use the `install` command:

```bash
$ sudo apt install <package-name>
$ sudo apt install firefox
```

To uninstall a pacakge, you can use the `remove` command:

```bash
$ sudo apt remove <package-name>
$ sudo apt remove firefox
```

Lastly, if you want to try finding a specific package, you have the `search` command:

```bash
$ sudo apt search <package-name>
$ sudo apt search firefox
```

## Conclusion

That covers the basics of package management in *Ubuntu*! In different distros, the way to install packages is most likely going to be different, unless it is another distro that also uses `apt`, such as *Debian*. That being said, the commands still remain similar. For instance, to install a package in *Fedora* you would use the `sudo dnf install <package>` command.