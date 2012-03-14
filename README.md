# convert-config

This project allows you to convert a configuration file in yaml, json or php format to each other of these formats. You may provide absolute or relative to current working directory file paths.

If you want to automatically overwrite the destination file when it exists use `--force` or `-f` option.

## Installation

    $ curl -s http://getcomposer.org/installer | php
    $ php composer.phar install

## Usage

To convert composer file from yaml to json, run:

    $ bin/convert-config yaml-to-json composer.yml composer.json

To convert composer file from json to yaml, run:

    $ bin/convert-config json-to-yaml composer.json composer.yml
