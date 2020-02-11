# Liquid Church's WordPress Guide

## Introduction
This repository provides an opinioniated guide to the use of WordPress at Liquid Church.

For more on why we use WordPress see our [Why WordPress document](WhyWordPress.md).

## Development

### Local Environment
There are many ways to setup a development environment for WordPress. In our experience one of the simplest and most mature is [Varying Vagrant Vagrants](https://varyingvagrantvagrants.org/) which uses [VirtualBox](https://virtualbox.org/) and [Vagrant](https://vagrantup.com).

For more on why we recommend VVV see [More On Local Environments](MoreOnLocalEnvironments.md).

### Version Control System
You should be using [GitHub](https://github.com/) for your code repositories and [Git](https://git-scm.com/) as your client/local repository host. Feel free to utilize a GUI based interface on top of the git software if you prefer (most IDE's have some support built-in).

We do use [Bitbucket](https://bitbucket.org/) to host our WP theme. This is legacy from when GitHub didn't offer free private repositories and Bitbucket did. It is likely we will eventually consolidate all repositories on GitHub.

### Integrated Development Environment
[JetBrain's PhpStorm](https://www.jetbrains.com/phpstorm/) is a nice IDE for PHP development which has specific integrations available for use with WordPress (and Vagrant). In our experience PhpStorm can be difficult to configure but overall is a worthwhile undertaking.

The other strong contender is [Visual Studio Code (VSC)](https://code.visualstudio.com/) which has a number of extensions that can provide WordPress support. The recently added remote development extensions which allow a near native experience on remote (or virtual) systems is fantastic.

For help configuring PhpStorm see [More On JetBrains PhpStorm](MoreOnJetBrainsPhpStorm.md).

### Unit Testing
We recommend using phpunit, IDE's generally integrate with it and it is the de facto standard. You can use WP-CLI to generate a generic set of unit tests you can customize.

### Code Quality
We recommend using php_codesniffer but with the PSR standards rather than WP standards.

### Continuous Integration
We are still working on this phase.

### WordPress Plugins
- [Query Monitor](https://querymonitor.com/) is an excellent (and free) plugin for seeing exactly how your WordPress code is working and can be very helpful in debugging.
- [What the File?](https://www.barrykooij.com/what-the-file/) is a useful extension that lets you see exactly which template files are being used to compose the page you are currently viewing.

## Theming
WordPress themes can be developed custom or a preexisting theme purchased and customized. There are a large number of free themes available in the [WordPress Theme Directory](https://wordpress.org/themes/). A popular paid source of themes is through [ThemeForest](https://themeforest.net/).

Our current site uses a custom built theme.

## Plugins
We use a number of plugins on our site. Some of these have been developed in-house (and are available free in our repositories). Some come from the [WordPress Plugin Directory](https://wordpress.org/plugins), some we have bought directly from vendors/developers, and some have been purchased through [CodeCanyon](https://codecanyon.net/).

Whenever we are looking to add new functionality to the site it is important for us to ask:
1. Are any pre-built solutions we can customize for our site available?
2. If a pre-built solution is available, do we trust that it has reliable and long-term support?
3. How will adding this plugin to our WP install affect performance, usability, and security?

## Putting It All Together
There is a lot here so we'll attempt to outline some of the basic steps below:
1. Follow instructions on setting up [VVV](MoreOnVVV.md).
2. Clone repositories you'll be editing into vvv/www/wordpress-one/public_html/wp-content/{plugins-or-themes}/{name-of-plugin-or-theme}.
3. Enter the project directory and if the project uses composer run `composer install`.
4. If the project uses npm run `npm install`.
5. Use phpunit.

## Other Notes
1. Much of the material here will apply to WordPress.com as well as the free/open WordPress, but we will not take the time to distinguish when certain features are not available on WordPress.com that are part of the free/open WordPress, nor will we cover functionality that is available via WordPress.com but not via the free/open WordPress. To learn more about the differences between WordPress.com and WordPress.org see [this WPMUdev article](https://premium.wpmudev.org/blog/wordpress-com-and-wordpress-org/).