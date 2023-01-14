oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g neon
$ neon COMMAND
running command...
$ neon (--version)
neon/0.0.0 darwin-x64 node-v19.3.0
$ neon --help [COMMAND]
USAGE
  $ neon COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`neon hello PERSON`](#neon-hello-person)
* [`neon hello world`](#neon-hello-world)
* [`neon help [COMMAND]`](#neon-help-command)
* [`neon plugins`](#neon-plugins)
* [`neon plugins:install PLUGIN...`](#neon-pluginsinstall-plugin)
* [`neon plugins:inspect PLUGIN...`](#neon-pluginsinspect-plugin)
* [`neon plugins:install PLUGIN...`](#neon-pluginsinstall-plugin-1)
* [`neon plugins:link PLUGIN`](#neon-pluginslink-plugin)
* [`neon plugins:uninstall PLUGIN...`](#neon-pluginsuninstall-plugin)
* [`neon plugins:uninstall PLUGIN...`](#neon-pluginsuninstall-plugin-1)
* [`neon plugins:uninstall PLUGIN...`](#neon-pluginsuninstall-plugin-2)
* [`neon plugins update`](#neon-plugins-update)

## `neon hello PERSON`

Say hello

```
USAGE
  $ neon hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/Makepad-fr/neon/neon/blob/v0.0.0/dist/commands/hello/index.ts)_

## `neon hello world`

Say hello world

```
USAGE
  $ neon hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ neon hello world
  hello world! (./src/commands/hello/world.ts)
```

## `neon help [COMMAND]`

Display help for neon.

```
USAGE
  $ neon help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for neon.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.22/src/commands/help.ts)_

## `neon plugins`

List installed plugins.

```
USAGE
  $ neon plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ neon plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.12/src/commands/plugins/index.ts)_

## `neon plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ neon plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ neon plugins add

EXAMPLES
  $ neon plugins:install myplugin 

  $ neon plugins:install https://github.com/someuser/someplugin

  $ neon plugins:install someuser/someplugin
```

## `neon plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ neon plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ neon plugins:inspect myplugin
```

## `neon plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ neon plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ neon plugins add

EXAMPLES
  $ neon plugins:install myplugin 

  $ neon plugins:install https://github.com/someuser/someplugin

  $ neon plugins:install someuser/someplugin
```

## `neon plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ neon plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ neon plugins:link myplugin
```

## `neon plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ neon plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ neon plugins unlink
  $ neon plugins remove
```

## `neon plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ neon plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ neon plugins unlink
  $ neon plugins remove
```

## `neon plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ neon plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ neon plugins unlink
  $ neon plugins remove
```

## `neon plugins update`

Update installed plugins.

```
USAGE
  $ neon plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
