# ILR Dev VM with [Drude](https://github.com/blinkreaction/drude) (**Dru**pal **D**ocker **E**nvironment)

## System requirements

Please review [system requirements](/docs/system-requirements.md) before proceeding with the setup.

<a name="setup"></a>
## Setup

1. [Drude environment setup](/docs/drude-env-setup.md)

    This is done **one time per host** and should be performed by everyone.

2. Clone the git repository for the ilr-website into this folder, which becomes your [projects folder](/docs/directory-structure.md)
3. `cd docroot`
4. `dsh up`
5. Once docker is finished building, type `dsh init` (this should sync the prod database to your system)
6. `dsh reload`


<a name="updates"></a>
## Updates

Switch to your `<projects>` folder and run:

```
dsh self-update
dsh update prerequisites
```

On Mac and Windows only (skip for Linux) also run:

```
dsh update boot2docker
```


<a name="dsh"></a>
## Drude Shell Helper (dsh)

Drude shell helper is a console tool that simplifies day-to-day work with Drude.
It provides a set of most commonly used commands and operations for controlling the Boot2docker VM, containers, running drush or other commands inside the **cli** container. (**Note**: dsh requires cli container to function properly)

See `dsh help` for a complete list.

`dsh` detects the environment it's launched in and will automatically start the boot2docker VM and launch containers as necessary.
It runs on Mac/Linux directly. On Windows `dsh` runs inside the Babun Shell.


<a name="cli"></a>
## Console tools (cli)

The **cli** container is meant to serve as a single console to access all necessary command line tools.
You can access **cli** container's console with `dsh`:

```
dsh bash
```

Tools available inside the **cli** container:

- php-cli, composer, drush[6,7,8], drupal console, phpcs
- ruby, bundler
- node, nvm, npm
- imagemagick
- python, git, mc, mysql-client and [more](https://github.com/blinkreaction/docker-drupal-cli)


<a name="instructions"></a>
## Instructions and tutorials

- [Drupal settings](/docs/drupal-settings.md)
- [Running multiple projects](/docs/multiple-projects.md)
- [Overriding default PHP/MySQL/etc. settings](/docs/settings.md)
- [Public access](/docs/public-access.md)
- [DB sandbox mode](/docs/db-sandbox.md)
- [Using Behat](/docs/behat.md)
- [Zero-configuration Debugging with Xdebug and PhpStorm](/docs/xdebug.md)
- [MySQL DB access for external tools](/docs/db-access.md)
- [Sending and capturing email](/docs/mail.md)
- [Enabling Varnish support](/docs/varnish.md)

<a name="troubleshooting"></a>
## Troubleshooting

See [Troubleshooting](/docs/troubleshooting.md) section of the docs.


## License

The MIT License (MIT)

Copyright (c) 2016 BlinkReaction

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
