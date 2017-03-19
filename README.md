# pdir2: Pretty dir() printing with joy🍺
[![Build Status](https://travis-ci.org/laike9m/pdir2.svg)](https://travis-ci.org/laike9m/pdir2)
[![Supported Python versions](https://img.shields.io/pypi/pyversions/pdir2.svg)](https://pypi.python.org/pypi/pdir2/)

Have you ever dreamed of a better output of `dir()`? I do. So I created this.

![](https://github.com/laike9m/pdir2/raw/master/images/presentation.gif)

## Features
* Attributes are grouped by types/functionalities, with beautiful colors.

* Support all platforms including Windows(Thanks to [colorama](https://github.com/tartley/colorama)).

* Support [ipython](https://github.com/ipython/ipython), [ptpython](https://github.com/jonathanslenders/ptpython) and [bpython](https://www.bpython-interpreter.org/)! See [wiki](https://github.com/laike9m/pdir2/wiki#repl-support) for more information.

* The return value of `pdir()` can still be used as a list of names.

* You can search for certain names with `.s()` or `.search()`:  

  ![](https://github.com/laike9m/pdir2/raw/master/images/search.gif)

  Search is case-insensitive by default. You can use `.search(name, case_sensitive=True)` to do case sensitive searching.

## Install
```
pip install pdir2
```
About the name. I wanted to call it "pdir", but there's already one with this
name on pypi. Mine is better, of course.

As a better alternative of `dir()`, it's more convenient to automatically import
pdir2 when launching REPL. Luckily, Python provides a way to do this.

In you `.bashrc`(or `.zshrc`), add this line:
```
export PYTHONSTARTUP=$HOME/.pythonstartup
```
Then, create `.pythonstartup` in your home folder. Add one line:
```
import pdir
```
Next time you launch REPL, `pdir()` is already there, Hooray!

## Testing
Simply run `pytest`, or use `tox` if you like.
