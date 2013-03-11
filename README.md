# Unity Completions
#### Package for [Sublime Text](http://www.sublimetext.com/)

This package adds auto-completions for [Unity](http://www.unity3d.com/) classes, variables and functions.
It works with all Unity-supported languages: JavaScript, C# and Boo.

## Usage

Simply start typing any Unity term or press Ctrl+Space.
After auto-completing a function name, use Tab to easily iterate through the parameters.

## Installation

### Package Control

The best way to install this package is using 
[Package Control](http://wbond.net/sublime_packages/package_control).
See [installation](http://wbond.net/sublime_packages/package_control/installation)
and [usage](http://wbond.net/sublime_packages/package_control/usage)
for help.
Choose to install the "Unity Completions" package.
Package Control will also keep you updated.

### Manual

Alternatively you can install this package manually:

1. Open the [packages directory](http://docs.sublimetext.info/en/latest/basic_concepts.html#the-packages-directory)
from the Sublime Text menu (Preferences | Browse Packages...)
2. Create a new directory called "Unity Completions"
3. Copy the contents of this package into the new directory

## Boo

In order for Sublime Text to recognize .boo files you need to install a separate package: Boo.
You can install it using Package Control or manually from [here](https://github.com/Shammah/boo-sublime).

## Generation

The _sublime-completions_ files were generated automatically using
[this generator](https://github.com/oferei/sublime-unity-completions-generator).
The data is based on the [Unity Scripting Reference](http://docs.unity3d.com/Documentation/ScriptReference/).
