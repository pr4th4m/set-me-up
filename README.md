### Set Me Up
Set up development machine instantly.


#### Compatibility
- Ubuntu 16.04
- Ubuntu 14.04


#### Pre-requisites
- Only for Ubuntu 16.04

        sudo apt-get install python python-dev

- Mandatory pre-requisites

        sudo apt-get install git python-pip
        pip install ansible==2.1

- Machine user should be a sudoers


#### Usage
- Clone repo

        git clone https://github.com/pratz/set-me-up.git

- Run below command to set up development machine

        cd set-me-up
        ansible-playbook -i inventory set_me_up.yml


#### What's configured ?
- Zsh with zim framework
- Tmux
- Neovim
- The silver searcher (Ag)
- Python utils like virtualenv, virtualenvwrapper etc


#### Post Installation
- After development machine is configured, open `nvim` and run below command to install neovim plugins

        :PlugInstall
        :UpdateRemotePlugins

- Make zsh default shell

        chsh -s $(which zsh)
