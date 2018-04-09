# WordPress Itself
WordPress is a Content Management System (CMS) written in HTML, CSS, PHP, and JavaScript. It is available for free and under an open source license from [WordPress.org](wordpress.org). It is the world's most widely used CMS and is utilized by well over 25% of the world's websites that utilize a CMS - from small blogs to the largest enterprises.

Matt Mullenweg is the de facto leader of WordPress, having started the [project in 2003 with Mike Little.](wordpress.org/about/) Matt is also CEO of Automattic which offers a number of WordPress products and services including [WordPress.com](wordpress.com), a hosted WordPress service. For the purposes of this article we will be focusing on the free and open source version of WordPress as opposed to that provided by Automattic at WordPress.com.<sup>1</sup>

# Why WordPress?
Why have we chosen to use WordPress instead of creating a bespoke CMS or utilizing any of the many other CMS options available?

1. It is the market leader for content management systems and as such has a tremendous ecosystem built around it including thousands of businesses that specialize in building bespoke solutions on top of WordPress.
1. It is open source, this means that we can view and change the source code as needed. Should WordPress be abandoned (not gonna happen) or should it go in a direction at odds with our needs we can always choose to *fork* the code and create our own implementation that is tailored to our needs (we have no intention of doing so).
1. It is extendable using themes and plugins - whether custom-built or from a third party. Many of these themes/plugins are also open source.
1. It provides a User Interface which is friendly to non-technical users but also has tremendous power under the hood that can be utilized by developers.

# WordPress 101 - Using WordPress
- Common Concepts
  - Post
  - Hierarchies (Categories, Tags)
  - Comments
  - Themes
  - Plugins
  - Widgets
  - Menus
  - Page
  - Homepage
  - Users
- Creating Pages and Posts
  - Categories and Tags
  - Adding Images
  - Videos and Other Media
  - Visual Editor and Text Editor
  - Drafts, Pending Articles, and Timestamps
- Advanced Page and Post Options
  - Excerpts
  - Comments/Discussions
  - Custom Fields
  - Post Revisions
  - Pretty Post Slug
- Comments/Discussion
  - Adding a Comment
  - Discussion Settings
  - Moderating Comments
  - Eliminating Comment Spam
- Page Specific
  - Choosing a Parent
  - Changing Order of Pages
- Media Library
  - Managing Media
  - Creating a Gallery
  
# WordPress 102 - Configuring and Extending WordPress as a User
- Installing and Configuring WordPress
  - Configuring Permalinks
  - Enabling HTTPS
- Themes
  - Finding a Theme
  - Installing a Theme
  - Customizer
  - Site Identity
  - Colors
  - Header Media
  - Background
  - Widgets
  - Static Front Page
  - Additional CSS
- Importing and Exporting Content
- Menus
  - Add a Menu
  - Display the Menu
- Widgets
- Plugins
  - What Are They?
  - Finding Them
  - Installing Plugins
  - Must Have Plugins
    - Backups
    - Google Analytics
    - Caching
    - SEO
    - Security
    - Social Media
    - Jetpack
 - Managing Users
  
# WordPress 201 - Theme Development
- Choose How You'll Build
  - Ground Up
  - Framework
  - Starter Theme
- Creating Theme Folder
- Creating Basic WordPress Contnet
  - functions.php
  - header and footer
  - sidebar
  - main content (the loop)
- Creating Template Files within Theme
  - Understanding WordPress Theme Structure
  - header.php
  - footer.php
  - sidebar.php
  - Archive
  - Single
  - Page
  - Generating Classes for Body and Post
  - Other Templates
  - Creating and Using a Custom Page Template
- Integrating Widget Compatibility
- Enabling a Menu
- Creating a Child Theme

# WordPress 202 - Plugin Development
- Creating a Basic Plugin
  - Naming and Organizing Files
  - Creating Functions
  - Adding Hooks
  - Testing
- Adding an Admin Page
- Integrating with the Database
- Creating Shortcodes
- Custom Post Types (CPTs)
- Custom Taxonomies

# WordPress 203 - REST API

# WordPress Optional 901 - Widget Development


# Themes
WordPress uses themes to customize the appearance of a WordPress instance. There are tens of thousands of themes available, some [free](wordpress.org/themes), some for [pay](themeforest.net). One can also build custom themes, but more on that later.

# Plugins
WordPress uses plugins to extend the default functionality of the CMS. There are tens of thousands of plugins available, many [free](wordpress.org/plugins/) and [paid](codecanyon.net).

# Notes
1. Much of the material here will apply to WordPress.com as well as the free/open WordPress, but we will not take the time to distinguish when certain features are not available on WordPress.com that are part of the free/open WordPress, nor will we cover functionality that is available via WordPress.com but not via the free/open WordPress. To learn more about the differences between WordPress.com and WordPress.org see [this WPMUdev article](https://premium.wpmudev.org/blog/wordpress-com-and-wordpress-org/).

# Bibliography
- I am greatly indebted to Karol Krol's Table of Contents in WordPress Complete Sixth Edition for thinking through and listing the different areas of functionality one needs to learn with WordPress.
