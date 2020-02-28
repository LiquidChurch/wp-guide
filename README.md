# Liquid Church's WordPress Guide

## Introduction
This repository provides an opinioniated guide to the use of WordPress at Liquid Church.

For more on why we use WordPress see our [Why WordPress document](WhyWordPress.md).

## Quick Overview
1. Setup Version Control System (git).
2. Setup Local Environment (VVV).
3. Setup IDE (PhpStorm or VSCode).
4. Setup Code Quality Tools (PHP_CodeSniffer).
5. Setup WordPress Developer Plugins.
6. Create/Clone Repositories.
7. Setup Package Management: Part 1 (Phive).
8. Setup Package Management: Part 2 (Composer).
8. Setup Package Management: Part 3 (npm).
9. Setup Unit Tests (PHPUnit).
4. Enter the project directory and if the project uses composer run `composer install`.
5. If the project uses npm run `npm install`.
6. Use phpunit for unit testing.

## Development

### Version Control System
You should be using [GitHub](https://github.com/) for your code repositories and [Git](https://git-scm.com/) as your client/local repository host. Feel free to utilize a GUI based interface on top of the git software if you prefer (most IDE's have some support built-in).

We use [Bitbucket](https://bitbucket.org/) to host our WP theme because we keep it in a private repo and GitHub does not offer organizations free private repos.

### Local Environment
There are many ways to setup a development environment for WordPress. In our experience one of the simplest, full-featured, and stablest is [Varying Vagrant Vagrants](https://varyingvagrantvagrants.org/) which uses [VirtualBox](https://virtualbox.org/) and [Vagrant](https://vagrantup.com).

For more on why we recommend VVV see [More On Local Environments](MoreOnLocalEnvironments.md).

For instructions on installing VVV see [More On VVV](MoreOnVVV.md).

### Integrated Development Environment
[JetBrain's PhpStorm](https://www.jetbrains.com/phpstorm/) is a nice IDE for PHP development which has specific integrations available for use with WordPress (and Vagrant). In our experience PhpStorm can be difficult to configure but once working is quite useful.

The other strong contender is [Visual Studio Code (VSC)](https://code.visualstudio.com/) which has a number of extensions that can provide WordPress support. The recently added remote development extensions which allow a near native experience on remote (or virtual) systems is fantastic.

For help configuring PhpStorm see [More On JetBrains PhpStorm](MoreOnJetBrainsPhpStorm.md).

### Code Quality
We recommend using [php_codesniffer](https://github.com/squizlabs/PHP_CodeSniffer) but with the PSR standards rather than WP standards.

### WordPress Plugins
- [Query Monitor](https://querymonitor.com/) is an excellent (and free) plugin for seeing exactly how your WordPress code is working and can be very helpful in debugging.
- [What the File?](https://www.barrykooij.com/what-the-file/) is a useful extension that lets you see exactly which template files are being used to compose the page you are currently viewing.
- Plugins are available for accessing the database but we recommend using the bundled phpMyAdmin, keeps the WP install slimmer.

### Create/Clone Repositories
- If you are starting a new project from scratch you'll want to create a repo on GitHub and clone that repo down to your local machine.
- If you are working on an existing repo you'll clone it to your local machine.
- You should clone into: vvv/www/wordpress-one/public_html/wp-content/{plugins-or-themes}
    - By default the github repo name will be used as the folder name.

### Package Management Tools
For PHP you'll want to install two package management applications. The first is [Phive](https://phar.io/). You can use this to install Composer and later PHPUnit.

The second is [Composer](https://getcomposer.org/), this is the most popular package management system for PHP, it can also generate autoload files for your project.

Once in your project directory you can run `composer install` to have composer execute its config.

You'll also need [Node.js](https://nodejs.org/en/) and [npm](https://www.npmjs.com/), the popular JS package management program. This one you can install at your OS level and at the VM level. You need the former if you want to use BackstopJS to perform visual regression testing.

### Unit Testing
We recommend using [phpunit](https://phpunit.de/), IDE's generally integrate with it and it is the de facto standard for PHP. You can use WP-CLI to generate a generic set of unit tests you can customize.

### Continuous Integration
We are still working on this phase.

## Theming
There are a large number of free themes available in the [WordPress Theme Directory](https://wordpress.org/themes/). A popular paid source of themes is through [ThemeForest](https://themeforest.net/).

Our current site uses a custom built theme.

## Plugins
We use a number of plugins on our site. Some of these have been developed in-house (and are available free in our repositories). Some come from the [WordPress Plugin Directory](https://wordpress.org/plugins), some we have bought directly from vendors/developers, and some have been purchased through [CodeCanyon](https://codecanyon.net/).

Whenever we are looking to add new functionality to the site it is important for us to ask:
1. Are any pre-built solutions we can customize for our site available?
2. If a pre-built solution is available, do we trust that it has reliable and long-term support?
3. How will adding this plugin to our WP install affect performance, usability, and security?

## Other Notes
- If using Windows and Git Bash it is helpful to add a few aliases to Git Bash. These are the same as those found in [More on VVV](MoreOnVVV.md) but with the path updated from `/srv/` to `/c/path/to/vvv/`.

## Footnotes
[1] Much of the material here will apply to WordPress.com as well as the free/open WordPress, but we will not take the time to distinguish when certain features are not available on WordPress.com that are part of the free/open WordPress, nor will we cover functionality that is available via WordPress.com but not via the free/open WordPress. To learn more about the differences between WordPress.com and WordPress.org see [this WPMUdev article](https://premium.wpmudev.org/blog/wordpress-com-and-wordpress-org/).