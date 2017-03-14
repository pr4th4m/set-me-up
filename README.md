### Set Me Up
Set up development machine instantly.


#### Compatibility
- Ubuntu 16.04
- Ubuntu 14.04


#### Pre-requisites
- Mandatory/Optional pre-requisites

        sudo apt-get update
        sudo apt-get dist-upgrade

        # Mandatory pre-requisites
        sudo apt-get install git libssl-dev python-dev python-pip
        sudo pip install ansible==2.1

        # Only for Ubuntu 14.04
        sudo pip install markupsafe


- Machine user should be a sudoers


#### Usage
- Clone repo

        git clone https://github.com/pratz/set-me-up.git

- Run below command to set up development machine

        cd set-me-up
        ansible-playbook -i inventory set_me_up.yml

        # specific programs
        ansible-playbook -i inventory set_me_up.yml --tags "zsh,neovim"

        # available tags
        "zsh,tmux,neovim,ag,py_utils"


#### What's configured ?
- Zsh with zim framework
- Tmux
- Neovim
- The silver searcher (Ag)
- Python utils like virtualenv, virtualenvwrapper etc


#### Post Installation
- Open `zsh` and run below command to install tmux plugins

        zplug install
        zplug load

- Open `tmux` and run below command to install tmux plugins

        prefix + I

- Open `nvim` and run below command to install neovim plugins

        :PlugInstall
        :UpdateRemotePlugins

- Make zsh default shell

        chsh -s $(which zsh)
