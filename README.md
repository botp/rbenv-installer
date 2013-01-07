rbenv installer
===============

This tool is used to install `rbenv` and some plugins. It also provides 
scripts to install required software to be able to compile **Ruby**.

Installed plugins are `rbenv-vars`, `ruby-build` & `rbenv-installer`.


Before Installing
-----------------

Install `git` and `curl`:

    sudo apt-get -y install git-core curl


Install
-------

Install [rbenv] and friends by running:

    curl https://raw.github.com/fesplugas/rbenv-installer/master/bin/rbenv-installer | bash


Installing a Ruby
-----------------

Install Ruby `1.9.3-p194` and make it global:

    rbenv install 1.9.3-p194
    rbenv global 1.9.3-p194


Updating
--------

Update `rbenv` and plugins provided by the installer running:

    rbenv update


Bootstrap
---------

If you are installing `rbenv` in Ubuntu you'll probably need to install
required packages first:

    rbenv bootstrap-ubuntu-12-04
    rbenv bootstrap-ubuntu-10-04

To update `RubyGems` and install `bundler` and `rake`:

    rbenv bootstrap


About rbenv
-----------

**rbenv** source code is available at <https://github.com/sstephenson/rbenv>

[rbenv]: https://github.com/sstephenson/rbenv
