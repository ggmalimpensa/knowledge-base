# Installation

OS: Linux Mint 20 (Ulyana)

Run below commands to install `pip` (package installer for python) and `virtualenvwrapper` (virtual environment manager)

    sudo apt update
    sudo apt install python3-pip
    sudo pip3 install virtualenv
    sudo pip3 install virtualenvwrapper

Then append below commands to `.bashrc` file

    # virtualenvwrapper
    export PIP_REQUIRE_VIRTUALENV=true
    export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
    export WORKON_HOME=$HOME/.virtualenvs
    source /usr/local/bin/virtualenvwrapper.sh

To create `test` virtual environment, run below command

    mkvirtualenv -a /path/to/project test

To remove `test` virtual environment, run below command

    rmvirtualenv test
