rbenv installer
===============

Before Installing
-----------------

1. Install `git`:

    apt-get -y install git-core

2. Make sure your user has `sudo` privileges.


Install
-------

Install [rbenv] and friends by running:

    curl -L https://raw.github.com/fesplugas/rbenv-installer/master/bin/rbenv-installer | bash

Installing a Ruby
-----------------

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

If you are installing `rbenv` in Ubuntu you'll probably need to install
required packages first:

    rbenv bootstrap-ubuntu-10-04
    rbenv bootstrap-ubuntu-11-04


About rbenv
-----------

**rbenv** source code is available at <https://github.com/sstephenson/rbenv>

[rbenv]: https://github.com/sstephenson/rbenv
