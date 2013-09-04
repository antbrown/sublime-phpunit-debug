# Overview

Run `phpunit-debug` to debug your unit tests in Sublime Text 2.

Requires:
 - Sublime Text 2
 - [martomo/SublimeTextXdebug](https://github.com/martomo/SublimeTextXdebug) Package
 - PHP5, Xdebug extension, PHPUnit

## Installation

The `bin/phpunit-debug` program runs `export XDEBUG_CONFIG="idekey=sublime.xdebug"`, make sure the `idekey` value is also set in the `[xdebug]` section of your `php.ini` file. A sample `[xdebug]` section with the `idekey` value set is provided in `xdebug-sample.ini`.

Make sure `bin/phpunit-debug` is on your `$PATH` somewhere and is executable.

_For example: Copy to your ~/bin folder and customize idekey value_

## Starting the Sample Debug Session

Open the file `tests/ExampleTest.php` in Sublime Text 2 and goto line 10: `$stack = array();`.

Hit `Cmd+F8` on OS X, or `Ctrl+F8`, to Add a Breakpoint at the current line. You can trigger this manually by opening the Command Palette and fuzzy-searching for `Xdebug: Add/Remove Breakpoint`. A dot should appear next to the line number in the gutter. 

Start Debugging by pressing `Ctrl+Shift+F9` or fuzzy-search `Xdebug: Start Debugging`. You will see the Debugging Layout appear.

Now in your Terminal, at the root of this git repo, type `phpunit-debug` to begin debugging the `StackTest` in Sublime Text 2.

## Known to work with...

 - OS X 10.8, Homebrew php54/php54-xdebug/phpunit, Sublime Text 2.0.2 build 2221

## Acknowledgements

I originally saw this being done on [Rafeal Dohms' blog](http://blog.doh.ms/), using NetBeans, see the [original post here](http://blog.doh.ms/2011/05/13/debugging-phpunit-tests-in-netbeans-with-xdebug/).
