# Installation

OS: Linux Mint 20 (Ulyana)

First, run below commmand to install `nvm` (node version manager), as explained in documentation (https://github.com/nvm-sh/nvm)

    wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash

This command downloads the nvm repository and appends the following lines to `.bashrc`

    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

To install the latest LTS version of node, run below command

    nvm install --lts

To list all installed versions, run below command

    nvm ls

To use a specific version of node, run below command

    nvm use <version>

To uninstall a specific version of node, the below command

    nvm uninstall <version>
