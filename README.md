# Unity Completions
#### Package for [Sublime Text](http://www.sublimetext.com)

This package provides auto-completions for [Unity](http://www.unity3d.com/) classes, variables and functions.
It works with all Unity-supported languages: JavaScript, C# and Boo.

There exists a <a href="https://github.com/oferei/sublime-unity-completions-light">lighter version</a> of this package.
The auto-completions pop-up menu shown by the light package is not as nice and informative,
but on the other hand the light package does not add any delay to Sublime Text's loading time.
If you open and close Sublime Text frequently, I recommend using the light version.

## Installation

### Package Control

The easiest way to install this package is using 
[Package Control](http://wbond.net/sublime_packages/package_control).
Choose to install the <b>"Unity Completions"</b> package.
(See [installation](http://wbond.net/sublime_packages/package_control/installation)
and [usage](http://wbond.net/sublime_packages/package_control/usage)
for help.)
Package Control will also keep you updated.

#### Troubleshooting

Package Control may get stuck while installing the library.
If that happens you'd see the animation running at the bottom indefinitely:

![Installing](http://oferei.github.io/sublime-unity-completions/installing-package.gif)

This seems to be a bug in Package Control.
I'm not sure what causes it - perhaps the relatively large size of this package.
You are welcome to try the following solutions:

1. Wait a little longer - it may take a few (3-5) minutes!
2. Restart Sublime Text and try again, this time standing on one foot
3. Check your user settings (Preferences.sublime-settings) and make sure the package is not listed under "ignored_packages"
4. Consider using <a href="https://github.com/oferei/sublime-unity-completions-light">Unity Completions Light</a>

### Manual

Alternatively you can install this package manually:

1. Open the [packages directory](http://docs.sublimetext.info/en/latest/basic_concepts.html#the-packages-directory)
from the Sublime Text menu (Preferences | Browse Packages...)
2. Create a new directory called "Unity Completions"
3. Copy the contents of this package into the new directory

## Usage

Simply start typing any Unity term or press Ctrl+Space.
You don't have to be accurate - a few consonants may be enough, preferably in the right order.

For example, type in <code>gbjact</code> and you will instantly be offered completions with these letters:

![gbjact](http://oferei.github.io/sublime-unity-completions/complete-gbjact.png)

Notice the type on the right side:
_[var]_ for variables, _[class]_ for classes or parentheses with parameter names for functions.

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

Up to date with Unity version 5.0.2.

## Generation

The _Unity Completions_ package files were generated automatically using
[this generator](https://github.com/oferei/sublime-unity-completions-generator).
The data is based on the [Unity Scripting Reference](http://docs.unity3d.com/Documentation/ScriptReference/).

### Boo Developers

Ahoy!

If you're developing in Boo, know that this package recognizes .boo files,
but I recommend installing the [Boo package](https://github.com/Shammah/boo-sublime)
as well if you're into syntax highlighting.

## License

(The MIT License)

Copyright (c) 2013 Ofer Reichman

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
