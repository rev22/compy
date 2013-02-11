`compy` is a wrapper to `composer` for Symfony2 projects, using an
easier to use YAML file.

You can.use `compy` just like `composer`, except you modify the
`compy.yml`, instead of the `composer.json`:

    alice@acme$ bin/compy --version
    Composer version aa1c093

The YAML format is easier to read, easier to write
and allows you to add comments, like in the following snippet:

    license: MIT
    require:
        symfony/yaml:      '>=2.0'     # This is a comment
        symfony/console:   '>=2.0'
        composer/composer:  dev-master

When run the first time, `compy` converts automatically any composer.json present.
If you modify your `composer.json`, `compy` will automatically notice
it when you invoke it, and convert it to `compy.yml`. `compy` backs up
the compy.yml to `compy.yml~compy~`, before any change is made. 

To install `compy`:
* copy the contents of the `bin/` directory to your symfony project's `bin/` or `app/` directory;
* add a dependency to `composer/composer` in your `composer.json` and run `composer install`
* make sure the composer tool is installed system-wide