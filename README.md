# rbenv installer

This tool is used to install `rbenv` and some plugins.
Plugin repo of fesplugas has been replaced by botp (since the former repo is no longer existing).

## Requirements

- Git
- Curl or wget


## Install

Install [rbenv] and friends by running:   

    curl https://raw.githubusercontent.com/botp/rbenv-installer/master/bin/rbenv-installer | bash

or using wget

   wget -qO - https://raw.githubusercontent.com/botp/rbenv-installer/master/bin/rbenv-installer | bash


## Finding a ruby version

	rbenv install --list


## Installing a Ruby

Install latest stable Ruby and make it global:

    rbenv install 2.5.1
    rbenv global 2.5.1


## Updating

Update `rbenv` and plugins provided by the installer running:

    rbenv update


## Bootstrap

If you are installing `rbenv` in Ubuntu you'll probably need to install
some required packages. You can use the provided `bootstrap` scripts.

    rbenv bootstrap-ubuntu-16-04


## About rbenv

**rbenv** source code is available at <https://github.com/sstephenson/rbenv>

[rbenv]: https://github.com/sstephenson/rbenv
