# Microserve Contribution Day

A Docksal based local environment for our Drupal contribution days at [Microserve][microserve].

It includes commonly used Docksal addons, and automates common tasks like cloning Drupal core, generating hash salts, copying and changing settings files and setting up PHPUnit for running automated tests.
This should simplify and speed up the setup process, allowing more time for people to focus on contribution tasks.

## Prerequisites

- [Docksal](https://docksal.io)
- [Git](https://git-scm.com)

## Local setup

1. Clone the repository into your Docksal projects directory (e.g. `~/Projects`), specifying the directory name and the Drupal version.

    ```
    git clone https://github.com/microserve-io/contribution-day.git --branch 8.7.x drupal87
    ```

1. Go into the `drupal87` directory.

1. Run the `fin init` command. This will start the Docksal containers, clone the specified version of core, copy in the static files, run `composer install` and `drush site-install`.

   Drupal itself will be cloned into a `drupal` directory. Ensure that you are within this directory when creating patch files.

1. Visit http://drupal87.docksal in your browser.

1. To run automated tests, use the `fin phpunit` command.

## License

MIT

## Credits

* [Oliver Davies](https://github.com/opdavies)
* [All contributors](https://github.com/microserve-io/contribution-day/graphs/contributors)

[microserve]: https://microserve.io
