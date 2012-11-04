# ServerGroveShellAliasBundle

The ServerGroveShellAliasBundle is a Symfony2 bundle that generates a list of shell aliases for commands registered in
the Symfony application. The list of aliases can then be included in /etc/bash_profile or ~/.profile configuration files
so the commands can be autocompleted with the tab key.


## Usage

    $ php app/console generate:shell:aliases
    $ php app/console generate:shell:aliases --prefix=myapp --php=/usr/local/bin/php --absolute

If the absolute option is defined, the aliases will include the absolute path of the Symfony application, so you can
call these commands from anywhere in the filesystem.

## Installation:

Add the bundle with Composer:

    $ php composer.phar require servergrove/shell-alias-bundle

    $ php composer.phar install

Enable it in your app/AppKernel.php

	public function registerBundles()
	{
		$bundles = array(
			...

			new ServerGrove\Bundle\ShellAliasBundle\ServerGroveShellAliasBundle(),
		);

		...
	}


## More information:

* [ServerGrove Blog](http://blog.servergrove.com/)
* [Follow ServerGrove @ Twitter](http://twitter.com/servergrove)
* [GitHub Downloads](http://github.com/servergrove)