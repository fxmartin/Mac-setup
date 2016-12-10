# Packer

[Packer](https://www.packer.io) is a tool for creating machine and container images for multiple platforms from a single source configuration.

Packer is easy to use and automates the creation of any type of machine image. It embraces modern configuration management by encouraging you to use automated scripts to install and configure the software within your Packer-made images. Packer brings machine images into the modern age, unlocking untapped potential and opening new opportunities.

Out of the box Packer comes with support to build images for Amazon EC2, CloudStack, DigitalOcean, Docker, Google Compute Engine, Microsoft Azure, QEMU, VirtualBox, VMware, and more. Support for more platforms is on the way, and anyone can add new platforms via plugins.

### Before we start

In order to simplify the installation process you should install homebrew-cask which provides a friendly homebrew-style CLI workflow for the administration of Mac applications distributed as binaries. Refer to [this](../Homebrew/Cask.md) article in order to install homebrew-cask.

### Install

Install Packer either [from the website](https://www.packer.io/downloads.html) or use homebrew for installing it :

```
$ brew install packer
```

After installing Packer, verify the installation worked by opening a new command prompt or console, and checking that packer is available:

```
$ packer
usage: packer [--version] [--help] <command> [<args>]

Available commands are:
    build       build image(s) from template
    fix         fixes templates from old versions of packer
    inspect     see components of a template
    push        push a template and supporting files to a Packer build service
    validate    check that a template is valid
    version     Prints the Packer version
```

Homebrew-cask installs VMware in a non-standard location ```/Users/user/Applications/VMware\ Fusion.app```, you need to specify the path to avoid an error. Add the following command to the bash_profile file:

```
export FUSION_APP_PATH=/Users/user/Applications/VMware\ Fusion.app
```

### Usage

A machine image is a single static unit that contains a pre-configured operating system and installed software which is used to quickly create new running machines. Machine image formats change for each platform. Some examples include AMIs for EC2, VMDK/VMX files for VMware, OVF exports for VirtualBox, etc.
