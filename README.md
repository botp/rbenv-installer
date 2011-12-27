rbenv install
=============

Install and/or update [rbenv] and friends by running:

    curl -L https://raw.github.com/fesplugas/rbenv-installer/master/bin/rbenv-installer | bash

Install Ruby `1.9.3-p0` and make it global:

    rbenv install 1.9.3-p0
    rbenv global 1.9.3-p0


Updating
--------

Once `rbenv-installer` has been run there will be a new command
available on `rbenv` which is used to update `rbenv`, plugins and
the installer itself:

    rbenv update


Bootstrap
---------

If you are installing `rbenv` in Ubuntu you need to install first the
following packages:

    # Update, install development tools and git:
    sudo apt-get update
    sudo apt-get -y install build-essential
    sudo apt-get -y install git-core

    # Extras for RubyGems and Rails:
    sudo apt-get -y install zlib1g-dev libssl-dev

    # Readline Dev on Ubuntu 10.04 LTS:
    sudo apt-get -y install libreadline5-dev

    # Readline Dev on Ubuntu 11.10:
    # sudo apt-get -y install libreadline-gplv2-dev


**rbenv** source code is available at <https://github.com/sstephenson/rbenv>

[rbenv]: https://github.com/sstephenson/rbenv
