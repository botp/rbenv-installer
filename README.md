rbenv installer
===============

This tool is used to install `rbenv` and some plugins. It also provides 
scripts to install required software to be able to compile **Ruby**.

Installed plugins are:

- rbenv-vars
- ruby-build
- rbenv-installer


Before Installing
-----------------

Install `git` and `curl`:

    apt-get -y install git-core curl

Make sure your user has `sudo` privileges.


Install
-------

Install [rbenv] and friends by running:

    curl -L https://raw.github.com/fesplugas/rbenv-installer/master/bin/rbenv-installer | bash

Installing a Ruby
-----------------

Install Ruby `1.9.3p125` and make it global:

    rbenv install 1.9.3p125
    rbenv global 1.9.3p125


Updating
--------

Update `rbenv` and plugins provided by the installer running:

    rbenv update


Bootstrap
---------

If you are installing `rbenv` in Ubuntu you'll probably need to install
required packages first:

    rbenv bootstrap-ubuntu-10-04
    rbenv bootstrap-ubuntu-11-10


About rbenv
-----------

**rbenv** source code is available at <https://github.com/sstephenson/rbenv>

[rbenv]: https://github.com/sstephenson/rbenv
