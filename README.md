# ZSH Alias Configurator Helper Script
### By Austin Slade Getz

The purpose of this project is to provide a simple quality of life update for aliasing in the shell.

## Setup 
If you do not have a `.zsh_alias` file in your home directory type 
```
cd ~
touch .zsh_alias
```
In order to run the script from your terminal type
```
source <pathto>/ZshAlias/alias_configurator
```
I highly suggest changing your `.zshrc` to run the script with argument 1, instead of `source ~/.zsh_alias`
In your `.zshrc` file replace `source ~/.zsh_alias` with `source <pathto>/ZshAlias/alias_configurator 1`

I also suggest adding `alias aliasing='source <pathto>/ZshAlias/alias_configurator'` in order to maximize workflow when quickly modifying aliases.

## Usage
Running `source ./alias_configurator` without any arguments will show the usage abilities of the script:
`Usage: <pathto>/ZshAlias/alias_configurator {0: set | 1: configure | 2: list | 3: edit alias | 4: edit this }`

Using the alias for the script (shown above), 
`aliasing 0` will set the aliases made without any feedback.

`aliasing 1` will set the aliases made with feedback and will echo `ALIASES CONFIGURED`.

`aliasing 2` will output the `.zsh_alias` file, i.e. show list of your aliases.

`aliasing 3` will open the `.zsh_alias` with vim, allowing you to edit your aliases.

`aliasing 4` will open the `alias_configurator` script with vim, allowing you to edit the script to change instances of vim with your favorite text editor and/or change the destination of each sourced file.


**The script currently assumes that `.zsh_alias` `ZshAlias/` are located in your home directory**

In order to use this script the files must be in the appropriate place, and in order to do this, open the script with a text editor and change all instances of `~` to the appropriate path.
