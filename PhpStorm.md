# More on JetBrain's PhpStorm IDE

[JetBrain's PhpStorm](https://www.jetbrains.com/phpstorm/) is one of the most powerful IDE's for WordPress Development. That said, we have found that it is sometimes difficult to configure. Hopefully tips we provide here will be helpful.

## Configure the Settings!
1. Before you start doing any work in PhpStorm make sure you configure the settings.
### Vagrant
2. Configure PhpStorm to use Vagrant as its development environment (Settings-->Tools-->Vagrant).
    - Instance folder will be the root of the vvv project, not the root of your plugin/theme. It will look something like `c:\code\vvv`.
### Default Code Location
3. Change the default directory for projects to wherever you keep your code, by default PhpStorm wants to put it in its own folder path which we haven't found helpful. (Settings-->Appearance & Behavior-->System Settings-->Default Directory)
### Open Entire WP Install
4. Open the entire WordPress installation as your project, not just the specific plugin/theme you are working on.*
### Other Configuration Settings
5. You'll want to create custom scopes for testing your projects. This is especially important if you have vendor files in your code (Settings-->Appearance & Behavior-->Scopes).
6. You can enable visible hard wrap, line numbers, indent guides, etc. in Settings-->Editor-->General-->Appearance.
7. We recommend against using the WP Coding Standards formatting PhpStorm offers, this is at odds with the PHP-FIG standards (PSR-2, etc.) and we recommend utilizing the latter.
8. By default PhpStorm wants to use the tab character when indenting, you want spaces (Settings-->Editor-->Code Style-->PHP).
9. PhpStorm does include tools for database management, use them if you wish. Oftentimes phpmyadmin which is included with VVV is sufficient.
10. The default inspections are fairly logical and useful although spelling errors throw a million errors. To avoid this make sure the custom liquid spelling dictionary is included with the project by adding it to Settings-->Editor-->Spelling-->Dictionaries.
11. Make sure your encoding is set to UTF-8 with NO BOM (Settings-->Editor-->File Encodings).
12. Make sure you review your settings under Settings-->Version Control-->Git and GitHub.
### Deployment Servers
13. Setup deployment servers under Settings-->Build, Execution, Deployment-->Deployment. Use SFTP.
    1.  Make sure to create the mappings, these mappings should go from the root of the wordpress install to the root of wordpress on the server. If using SiteGround you'll use something like /name.liquidchurch.com/public_html, on some older SG hosts you may need to open File Manager through SG's control panel to see the full path you'll need as by default SG doesn't drop you into the correct directory but also doesn't let you traverse directories.
### Including Libraries
14. You'll probably want to include jquery and grunt libraries so that PhpStorm doesn't yell at you every time you use them. This can be accomplished in Settings-->Languages & Frameworks-->JavaScript-->Libraries. On the right hand side of the window choose Download and select the desired library.
### Code Quality for JS
15. We recommend installing jshint and configuring it (Settings-->Languages & Frameworks-->JavaScript-->Code Quality Tools-->JSHint).
    1.  We also recommend setting ESLint (same settings path) to Automatic.
### Configure PHP / Xdebug
16. Make sure you configure PHP (Settings-->Languages & Frameworks-->PHP)
    1.  For language level set to 7.2+ but not the latest version as the web host may not yet provide it.
    2.  The CLI interpreter should point to your VVV instance, when adding a new interpreter to the list Vagrant will be an option.
    3.  Make sure you setup Xdebug, it is included with VVV but not enabled.
        1.  Sometimes Xdebug can be finicky. Try ensuring that you have PhpStorm set to listening and installing the JetBrains IDE Support extension in your browser.
        2.  You'll want to exclude the main WP files unless you think the bug is in the core WP code. This is unlikely. By skipping the WP core files you'll keep the debugger focused on your code (Settings-->Languages & Frameworks-->PHP-->Debug-->Step Filters)
### Check Server Settings
17. Hopefully under Settings-->Servers, PhpStorm will automatically populate the VVV server.
    1.  Make sure the paths are correct and that use path mappings is checked.
### Configure Phive and Composer
18. If needed, configure composer (Settings-->Languages & Frameworks-->PHP-->Composer).
19. We recommend utilizing PHPUnit (PHP-->Test Frameworks). Use PHIVE to install phpunit.
    1.  You may need to set the path for phpunit.phar, after using PHIVE to include it in your project it should be found under wordpress_instance/public_html/wp-content/path-to-project/tools/phpunit.
### Code Quality for PHP
20. One can use quality tools like PHP_CodeSniffer however if you aren't starting with a fresh codebase the number of errors generated by PHP_CodeSniffer seems to be overwhelming and unhelpful.
### Enable WP Integration
21. Make sure that WP integration is enabled under Settings-->Languages & Frameworks-->PHP-->Frameworks-->WordPress. The path should point to the base of your WordPress install.


* Trust us. We've spent innumerable hours trying to get PhpStorm to work scoped to a specific code project and using the WP install as an additional resource, etc. Sometimes it seems like it will work, or works a tiny bit, but expect more headaches to be soon approaching.