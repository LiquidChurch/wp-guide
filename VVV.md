# Using Varying Vagrant Vagrants (VVV)
There are many ways to setup a development environment for WordPress. In our experience one of the simplest, full-featured, and stablest is [Varying Vagrant Vagrants](https://varyingvagrantvagrants.org/) which uses [VirtualBox](https://virtualbox.org/) and [Vagrant](https://vagrantup.com).

For more on why we recommend VVV see [More On Local Environments](MoreOnLocalEnvironments.md).

VVV is a Vagrant configuration specifically optimized for WordPress development. It takes between 15-30 minutes for the mainly automated process to be setup initially.

## Installation
See the [official VVV docs on setting up VVV](https://varyingvagrantvagrants.org/docs/en-US/installation/software-requirements/). Some key things to remember:
1. You'll need to install [VirtualBox](https://virtualbox.org) and [Vagrant](https://vagrantup.com/) before using VVV.
2. You should download VVV via git (`git clone https://github.com/Varying-Vagrant-Vagrants/VVV.git`).
3. You should install the vagrant-hostsupdater plugin (you'll be prompted when you execute `vagrant up` for the first time).
4. The configuration of VVV is specified in the config/config.yml file. This can be safely edited as it will not be overwritten when pulling a newer version of VVV from github.
    - When you first run `vagrant up`, vagrant makes a copy of the config/default-config.yml as config/config.yml, this is how you are able to use git to pull down the latest version without overwriting the config.
5. The first time you run VVV it will perform some work in the background creating the box and configuring it for you. You may need to enter administrator credentials during this process.
6. If on Windows you'll need to **Run As Administrator** your preferred terminal, otherwise certain VVV related steps will fail.

## Basic Commands
To run VVV you need to be within the VVV folder (or one of its children folders).

- Start VVV: `vagrant up`
- Stop VVV: `vagrant halt`
- View Dashboard: https://vvv.test/
- WP Preinstalled Instance One: https://one.wordpress.test/
- WP Preinstalled Instance Two: https://two.wordpress.test/

## Reprovisioning
If you make changes to VVV's configuration you'll need to halt the box then run `vagrant up --provision`.

If things are really messy you can destory the virtual machine: `vagrant destroy`.

## Updating
There are several different components one can update when working with VVV:
1. Vagrant - the software that manages virtual machines for you.
2. VirtualBox - the virtual machine provider that actually hosts the virtual machines.
3. VVV - the git repository that contains a Vagrantfile and associated files for defining the VM that Vagrant creates and VirtualBox uses.
4. Boxes - VVV is built on top of a VirtualBox image. This image occasionally receives updates which can be applied.

## Customizing
You can customize your environment by editing `~/.bashrc` in VVV.

Particularly recommend:
```bash
export lqdnotes=/srv/www/wordpress-one/public_html/wp-content/plugins/lqd-notes
export lqdmessages=/srv/www/wordpress-one/public_html/wp-content/plugins/lqd-messages
export lqdfunctions=/srv/www/wordpress-one/public_html/wp-content/plugins/lqd-messages-fns
export lqdtheme=/srv/www/wordpress-one/public_html/wp-content/themes/liquidchurch
```

NOTE: DO NOT include ```bash ``` when pasting into .bashrc!!! This can cause infinite loop of bash shells being created.

These folders can then be navigated to quickly by entered `cd $lqdnotes` etc.

Before these aliases will work you'll need to rerun the bashrc file `source ~/.bashrc`.
