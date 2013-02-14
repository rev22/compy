`compy` is a wrapper to `composer` for Symfony2 projects, based on an
easier to use YAML file.

## Usage

You can use `compy` just like `composer`, except you modify the
`compy.yml`, instead of the `composer.json`:

    alice@acme$ bin/compy --version
    Composer version aa1c093

You should only run `compy` from the directory your `compy.yml` or `composer.json` are.
    
### Your `compy.yml`

The YAML format is easier to read, easier to write
and allows you to add comments, like in the following snippet:

    license: MIT
    require:
        symfony/yaml:      '>=2.0'     # This is a comment
        symfony/console:   '>=2.0'
        composer/composer:  dev-master

## (Automatic) Configuration

When run the first time, `compy` converts automatically any composer.json present.
If you modify your `composer.json`, `compy` will automatically notice
it when you invoke it, and convert it to `compy.yml`. `compy` backs up
your `compy.yml` to `compy.yml~compy~`, before any change is made. 

## Installation

System-wide installation is not supported at the moment.

You can install `compy` in your project by copying files by hand, or through `composer`:

### installing via composer
1. require the package `rev22/compy` via `composer`

        composer require rev22/compy:dev-master

2. copy the files to your project's `bin` or `app` directory:

        cp -uav vendor/rev22/compy/bin/* bin/

### copying files by hand:
1. copy the contents of the `bin/` directory to your symfony project's `bin/` or `app/` directory;
2. add a dependency to `composer/composer` in your `composer.json` and run `composer install`
3. make sure the composer tool is installed system-wide

## License

`compy` is available under the terms of a MIT-style license.   Please consult the file LICENSE

## History of the tool

The `compy` script was brought to you by Michele Bini.
The package includes on Oleg Stepura's `convert-config` tool, which was forked from Igor Wiedler's `composer-yaml`.

