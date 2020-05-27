# Testing Code

## Unit Tests
We recommend using [phpunit](https://phpunit.de/), IDE's generally integrate with it and it is the de facto standard for PHP. You can use WP-CLI to generate a generic set of unit tests you can customize.

- To install tests: `sudo bin/install-wp-tests.sh wptest root root localhost`
	- Installs wordpress at /tmp/wordpress (this is why you need `sudo`).
	- Creates /tmp/wordpress-tests-lib (pulls from wordpress.org /tags/5.3.2/tests/phpunit/includes and /data
	- Creates a MySQL DB that is called wptest with username/pass of root on the localhost (Vagrant VM).
	- Should install required plugins at /tmp/wordpress/wp-content/plugins but instead seems to install in actual plugin dir.
- To run: `phpunit`

## Visual Regression Tests
You can use BackstopJS for this purpose. You'll need to install it on your local OS so that it can capture screenshots of the pages you are testing.