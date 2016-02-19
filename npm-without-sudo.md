# How to install npm packages without sudo

You can set the prefix for npm packages (it is property named prefix) which controls where the global node modules get installed. Issue the following command to set the prefix 

`npm config set prefix '~/.npm-packages'`

and adding $HOME/.npm-packages/bin to $PATH by appending to .bashrc

`export PATH="$PATH:$HOME/.npm-packages/bin"`

Main link can be found [here](http://stackoverflow.com/questions/19352976/npm-modules-wont-install-globally-without-sudo)
