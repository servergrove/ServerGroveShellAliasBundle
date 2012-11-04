# ServerGroveShellAliasBundle

The ServerGroveShellAliasBundle is a Symfony2 bundle that generates a list of shell aliases for commands registered in
the Symfony application. The list of aliases can then be included in /etc/bash_profile or ~/.profile configuration files
so the commands can be autocompleted with the tab key.


## Usage

    $ php app/console generate:shell:aliases
    $ php app/console generate:shell:aliases --prefix=myapp --php=/usr/local/bin/php --absolute

The list of aliases that it generates would look like this:

    alias console-help="php app/console help"
    alias console-list="php app/console list"
    alias console-assets-install="php app/console assets:install"
    alias console-cache-clear="php app/console cache:clear"
    alias console-cache-warmup="php app/console cache:warmup"
    alias console-config-dump-reference="php app/console config:dump-reference"
    alias console-container-debug="php app/console container:debug"
    alias console-router-dump-apache="php app/console router:dump-apache"
    alias console-router-debug="php app/console router:debug"
    alias console-router-match="php app/console router:match"
    alias console-server-run="php app/console server:run"
    alias console-translation-update="php app/console translation:update"
    alias console-init-acl="php app/console init:acl"
    alias console-twig-lint="php app/console twig:lint"
    alias console-swiftmailer-spool-send="php app/console swiftmailer:spool:send"
    alias console-assetic-dump="php app/console assetic:dump"

Then, you can start typing the name of the command and auto-complete with the tab key: console-s[TAB] will complete to
console-server-run.

If the absolute option is defined, the aliases will include the absolute path of the Symfony application, so you can
call these commands from anywhere in the filesystem.

## Installation:

Add the bundle with Composer:

    $ php composer.phar require "servergrove/shell-alias-bundle dev-master"

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