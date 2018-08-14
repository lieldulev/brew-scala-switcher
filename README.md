> _IMPORTANT: homebrew switched to using a single recipe for scala, no need for this package anymore, use `brew switch` moving forward_

brew-scala-switcher
===================

A utility script to switch between Scala version on OSX that were installed using Homebrew. (Supports 2.9, 2.10, 2.11, 2.12)

> IMPORTANT: This script assumes you have 
>
> 1. Installed scala using `brew install scala` (or scala211, or scala210, or scala29) to the default location `/usr/local/Cellar/`. 
> 2. You are using Bash (this was not tested on Zsh)

## 3 Step Installation

`scswitch` is just a BASH shell script.

1. Grab `scswitch` and put it somewhere that is included in your PATH.
2. If it isn't marked as executable, type  `chmod +x scswitch` to make it so.
3. I lied, there is no 3rd step. 

##Usage
 
###List installed versions of scala

    $> scswitch 
    
    Scala Switch Script
    
    Usage: scswitch [VERSION]
    
    VERSION - Supports versions 2.9.*, 2.10.*, 2.11.* and 2.12.*
    
    Installed Versions:
    
    2.12.1 - Type 'scswitch 2.11' to switch to this version.
    2.11.8 - Type 'scswitch 2.11' to switch to this version.
    
###Switching to a specific version

    $> scswitch 2.11
    Switchd to:  /usr/local/Cellar/scala211/2.11.8

## Why?

Since scala is not a single versioned recipe right now, you can't use `brew switch` like you would normally do.

## How?

Look at the script, it is dead simple (this README.md has more text than the actual script) - all it does is change the needed symlinks in `/usr/local/bin`

## License
None. Public Domain. Do whatever you want.

## Warranty
None. Don't come looking for me.
