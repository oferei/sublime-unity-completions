# Unity Completions
#### Package for [Sublime Text](http://www.sublimetext.com)

This package provides auto-completions for [Unity](http://www.unity3d.com/) classes, variables and functions.
It works with all Unity-supported languages: JavaScript, C# and Boo.

## Installation

### Package Control

The easiest way to install this package is using 
[Package Control](http://wbond.net/sublime_packages/package_control).
Choose to install the <b>"Unity Completions"</b> package.
(See [installation](http://wbond.net/sublime_packages/package_control/installation)
and [usage](http://wbond.net/sublime_packages/package_control/usage)
for help.)
Package Control will also keep you updated.

### Manual

Alternatively you can install this package manually:

1. Open the [packages directory](http://docs.sublimetext.info/en/latest/basic_concepts.html#the-packages-directory)
from the Sublime Text menu (Preferences | Browse Packages...)
2. Create a new directory called "Unity Completions"
3. Copy the contents of this package into the new directory

## Usage

Simply start typing any Unity term or press Ctrl+Space.
After auto-completing a function name use Tab to easily iterate through the parameters.

For example, type in <code>gbjact</code> and you will instantly be offered completions with these letters:

![gbjact](http://oferei.github.io/sublime-unity-completions/complete-gbjact.png)

Notice the type on the right side. Function types include parameter names.

Another example. Type in <code>pscast</code> and you will be offered:

![pscast](http://oferei.github.io/sublime-unity-completions/complete-pscast.png)

Notice that functions may appear multiple times if they have several definitions.
They can be distinguished by the parameter names.
(The pop-up is too small to include the types...)

Once you select a _function_ completion, a full snippet will be inserted,
including the parameter types, names and default values:

![SphereCast](http://oferei.github.io/sublime-unity-completions/func-spherecast2.png)

You can then use Tab and Shift+Tab to quickly navigate between the parameters.

### Limitations

The _Unity Completions_ plugin is simple.
It does not analyze the code to detect variable types.
It only relies on the word being typed.
In addition, Sublime Text's auto-complete is interrupted by dots.
Typing in a dot will cause Sublime Text to ignore anything before the dot.

Let's say, for example, that you have a variable named <code>enemy</code> of type <code>GameObject</code>
and you want assistance writing <code>enemy.activeInHierarchy</code>.
Typing <code>enemy.</code> (with a dot) will not work.
As soon as you type in the dot the completions pop-up will close.

If you continue typing after the dot, for example <code>enemy.activein</code>,
you will be presented with completions,
but they will only be based on the part after the dot: <code>activein</code>.

Suppose you choose the completion <code>activeInHierarchy</code>,
you will end up with: <code>enemy.GameObject.activeInHierarchy</code>.
The class name is inserted together with the variable name.
Simply delete the class name manually.

## Status

Up to date with Unity version 4.3.1.

## Generation

The _Unity Completions_ package files were generated automatically using
[this generator](https://github.com/oferei/sublime-unity-completions-generator).
The data is based on the [Unity Scripting Reference](http://docs.unity3d.com/Documentation/ScriptReference/).
