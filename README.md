# BASHCDShortcut
BASH/ZSH command for changing directory to a folder at ~/Desktop (Mac)


## Setup
Add the following to .bashrc (or .zshrc if using ZSH)

> gt() { \
>&nbsp;&nbsp;cd ~/Desktop/"$1" \
>}

In Terminal/Shell run \
`source .bashrc` (or `. .zshrc` for ZSH)

This will tell the Terminal about your new command

## Try it out
Now run `gt /folder_on_your-desktop` to navigate to a folder on your Desktop 
without having to type the full `cd ~/Desktop/folder-on_your_desktop`

I called the function "gt" since I want to "go to" a folder on my desktop. 
You can change the name of the command by renaming the function in your .bashrc (or .zshrc)

Likewise, you can change the default path by editing `~/Desktop/`

`"$1"` is the parameter passed to the function. Feel free to edit/remove the parameter for your needs

Every time you change the function, you will need to re-run `source .bashrc` 
so the shell knows it has changed

## Move this function out of .bashrc
Here are directions for creating a separate file in which to place functions so you don't clutter your .bashrc/.zshrc

https://github.com/BrockNicholas/CustomShellFunction

## Get rid of it
To remove the function from your shell:
`unset -f gt`
