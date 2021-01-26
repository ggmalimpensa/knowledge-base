# Installation

OS: Linux Mint 20.1 (Ulyssa)

Run below command to install `pyenv` (simple python version management)

    curl https://pyenv.run | bash

Then append below commands to `.bashrc` file

    # pyenv
    export PATH="/home/gabriel/.pyenv/bin:$PATH"
    eval "$(pyenv init -)"
    eval "$(pyenv virtualenv-init -)"

Install below dependencies before install any version of python using pyenv

    sudo apt update
    sudo apt install libbz2-dev libffi-dev libreadline-dev libsqlite3-dev libssl-dev python-openssl zlib1g-dev

This step is a workaround to pyenv detect the system version of python (`pyenv` demands a binary called `python` in `/usr/bin/`, but this distro doesn't have it)

    cd /usr/bin/
    sudo ln -s python3 python

To install python `3.8.7`, run below command

    pyenv install 3.8.7

To test if pyenv is ok, run below command

    pyenv versions

Run below commands to install `pip` (package installer for python) and `virtualenvwrapper` (virtual environment manager)

    sudo apt update
    sudo apt install python3-pip
    sudo pip3 install virtualenv
    sudo pip3 install virtualenvwrapper

Then append below commands to `.bashrc` file

    # virtualenvwrapper
    export PIP_REQUIRE_VIRTUALENV=true
    export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python
    export WORKON_HOME=$HOME/.virtualenvs
    source /usr/local/bin/virtualenvwrapper.sh

To create `test` virtual environment, run below command

    mkvirtualenv -a /path/to/project test

To remove `test` virtual environment, run below command

    rmvirtualenv test
