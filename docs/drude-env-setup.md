# Drude environment setup

**This is a one time setup.**
Once you have a working Drude environment in place, you can use it for all Drude powered projects.

## Setup

1. Install `dsh` (Drude Shell)

    ```
    sudo curl -L https://raw.githubusercontent.com/blinkreaction/drude/master/bin/dsh  -o /usr/local/bin/dsh
    sudo chmod +x /usr/local/bin/dsh
    ```

2. Install Drude's prerequisites

    Mac and Windows: virtualbox, vagrant, boot2docker-vagrant
    Linux: docker, docker-compose

    It is recommended to remove any previous versions of these before proceeding.

    ```
    dsh install prerequisites
    dsh install boot2docker
    ```

    On Mac and Windows you should see two files created in the `projects` folder:

    ```
    Vagrantfile
    vagrant.yml
    ```

    Run `git diff` to make sure that the above scripts did not modify those files. If they were modified and the values are now incorrect, `git checkout .`
