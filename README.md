'compy' is a wrapper to 'composer' for Symfony2 projects, using an
easier to maintain YAML file.

You can.use 'compy' like you would 'composer', except you modify the
'composer.yml'.  The YAML format is easier to read, easier to write
and allows you to add comments.

When run the first time, 'compy' converts automatically any composer.json present.
If you modify your 'composer.json', 'compy' will automatically notice
it when you invoke it, and convert it to 'composer.yml'. 
'compy' backs up the composer.yaml to 'composer.yaml~compy~', before
any change is made. 

To install 'compy':
* copy the contents of the 'bin/' directory to your symfony project's 'bin/' or 'app/' directory;
* add a dependency to 'composer/composer' in your 'composer.json' and run 'composer install'
* make sure the composer tool is installed system-wide