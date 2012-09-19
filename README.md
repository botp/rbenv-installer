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


Patch: Ruby Packages
--------------------

Install patched `ruby-build` by using the following command:

    rbenv patch-ruby-build

Now when you install a new `Ruby` it will try to download a package
from a `RUBY_PACKAGE_REPO`. If no packages available it will compile
the package as usual.

    export RUBY_PACKAGE_REPO=https://www.strongspace.com/shared/lxc1jwhowa

You can always add the previous `export` into your `.bashrc` to install
always from that package repo.


Patch: rbenv-rehash-system
--------------------------

Imagine you are using Ruby 1.9.3-p0 which is now provided by `Ubuntu 12.04-LTS`
and you still want to be able to use `rbenv vars`. This is not possible with
`rbenv` and this is why we created `rbenv-rehash-system` which is a patched
version of the `rbenv-rehash` script provided by `rbenv`.

You can run it manually but everytime you open a new shell system shims will
dissapear if you do not install a Ruby with `rbenv`. You can force the creation
of system shims using:

    if [ -d "${RBENV_ROOT}" ]; then
      export PATH="${RBENV_ROOT}/bin:${PATH}"
      eval "$(rbenv init -)"
      eval "$(rbenv rehash-system)"
    fi

Created system shims are: `ruby`, `irb` and `bundler`.


About rbenv
-----------

**rbenv** source code is available at <https://github.com/sstephenson/rbenv>

[rbenv]: https://github.com/sstephenson/rbenv
