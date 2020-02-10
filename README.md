# Liquid Church's WordPress Guide

## Introduction
This repository provides an opinioniated guide to the use of WordPress at Liquid Church.

## Development

### Local Environment
There are many ways to setup a development environment for WordPress. In our experience one of the simplest and most mature is [Varying Vagrant Vagrants](https://varyingvagrantvagrants.org/) which uses [VirtualBox](https://virtualbox.org/) and [Vagrant](https://vagrantup.com).

For more on why we recommend VVV see [More On Local Environments](https://github.com/LiquidChurch/wp-guide/blob/master/MoreOnLocalEnvironments.md).

### Integrated Development Environment
JetBrain's PhpStorm is a nice IDE for PHP development which has specific integrations available for use with WordPress (and Vagrant). In our experience PhpStorm can be difficult to configure but overall is a worthwhile undertaking.

The other strong contender is Visual Studio Code (VSC) which has a number of extensions that can provide WordPress support. The recently added remote development extensions which allow a near native experience on remote (or virtual) systems is fantastic.

### WordPress Plugins
- Query Monitor is an excellent (and free) plugin for seeing exactly how your WordPress code is working and can be very helpful in debugging.