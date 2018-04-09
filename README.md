# WordPress Itself
WordPress is a Content Management System (CMS) written in HTML, CSS, PHP, and JavaScript. It is available for free and under an open source license from [WordPress.org](wordpress.org). It is the world's most widely used CMS and is utilized by well over 25% of the world's websites that utilize a CMS - from small blogs to the largest enterprises.

Matt Mullenweg is the de facto leader of WordPress, having started the [project in 2003 with Mike Little.](wordpress.org/about/) Matt is also CEO of Automattic which offers a number of WordPress products and services including [WordPress.com](wordpress.com), a hosted WordPress service. For the purposes of this article we will be focusing on the free and open source version of WordPress as opposed to that provided by Automattic at WordPress.com.<sup>1</sup>

# Why WordPress?
Why have we chosen to use WordPress instead of creating a bespoke CMS or utilizing any of the many other CMS options available?

1. It is the market leader for content management systems and as such has a tremendous ecosystem built around it including thousands of businesses that specialize in building bespoke solutions on top of WordPress.
1. It is open source, this means that we can view and change the source code as needed. Should WordPress be abandoned (not gonna happen) or should it go in a direction at odds with our needs we can always choose to *fork* the code and create our own implementation that is tailored to our needs (we have no intention of doing so).
1. It is extendable using themes and plugins - whether custom-built or from a third party. Many of these themes/plugins are also open source.
1. It provides a User Interface which is friendly to non-technical users but also has tremendous power under the hood that can be utilized by developers.

# Themes
WordPress uses themes to customize the appearance of a WordPress instance. There are tens of thousands of themes available, some [free](wordpress.org/themes), some for [pay](themeforest.net). One can also build custom themes, but more on that later.

# Plugins
WordPress uses plugins to extend the default functionality of the CMS. There are tens of thousands of plugins available, many [free](wordpress.org/plugins/) and [paid](codecanyon.net).

# Concepts
There are lots of terms and concepts you'll want to become familiar with - posts, pages, permalinks, page errors, and so on.



1. Much of the material here will apply to WordPress.com as well as the free/open WordPress, but we will not take the time to distinguish when certain features are not available on WordPress.com that are part of the free/open WordPress, nor will we cover functionality that is available via WordPress.com but not via the free/open WordPress. To learn more about the differences between WordPress.com and WordPress.org see [this WPMUdev article](https://premium.wpmudev.org/blog/wordpress-com-and-wordpress-org/).
2. This is something we should do when we have time.
3. We do use functions.php, but any significant functionality should be placed into its own plugin.
4. We use TinyMCE Advanced and an HTML Editor Syntax Highlighter.
5. I've mainly used Relevanssi in the past. Its admin UI isn't ideal and the use of this or any other search plugin needs to be carefully configured to work with our existing plugins - especially the messages plugin.
6. We currently use Bootstrap, though Twig/Timber are interesting and may be worth considering at some juncture.
7. I am all for visual page builders but strongly suggest that they output standard code/content that is not tied to the specific visual page builder, otherwise one becomes locked into a specific page builder since removing it will cause the site to break.
8. Alternatively, one can use Cloud9 (free) or DigitalOcean ($5/mo.) to spin up an instance.
