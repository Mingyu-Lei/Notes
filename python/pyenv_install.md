# Guide to install pyenv on a new Ubuntu machie

Reference: [Pyenv on github][Pyenv]   
	
[Pyenv]: https://github.com/pyenv/pyenv 

> Note: This guide is mainly for __Ubuntu__ with __bash__ shell, check the official guide for other combinations.

## 1. Change shell to bash
1. Type:

       sudo chsh -s /bin/bash
2. Then restart the shell

## 2. Get pyenv package
May change the loc where it will be installed

    git clone https://github.com/pyenv/pyenv.git ~/.pyenv

## 3. Define environment variable 

`PYENV_ROOT` to point to the path where pyenv repo is cloned and add `$PYENV_ROOT/bin` to your `$PATH` for access to the pyenv command-line utility.

For __bash__ only:

    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile

## 4. Add pyenv init to your shell

    echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile

## 5. Restart the shell so the path changes take effect.

    exec "$SHELL"

## 6. Install Python build dependencies
Note: For __Ubuntu__ mainly

For other environment, go to: [Suggested Environment][Env]   
	
[Env]: https://github.com/pyenv/pyenv/wiki#suggested-build-environment  

    sudo apt-get update; sudo apt-get install --no-install-recommends make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

## 7. Install Python versions into `$(pyenv root)/versions`

    pyenv install 3.6.8