## pyreadline3 fork

This project is a fork of [pyreadline3](https://github.com/pyreadline3/pyreadline3).

**Background:**
- **pyreadline3**: An updated version of [pyreadline](https://github.com/pyreadline/pyreadline), which was created when pyreadline became inactive in 2014.
- **Current Status**: Unfortunately, pyreadline3 has also become inactive, with pull requests pending since 2022.

**Needed Updates:**
- The official [GNU readline](https://tiswww.case.edu/php/chet/readline/rltop.html), is still under activate development and includes ANSI escape sequences that neither pyreadline nor pyreadline3 currently support.
- A package that I use, uses the official GNU readline and therefore uses ansi escape sequences that neither pyreadline nor pyreadline3 had defined.

Therefore, the only purpose of this fork is to add these needed keys.

This does not in any way make this fork a complete implementation of readline, it only adds minor things to pyreadline3.

Any bug fixes or new features should probably still be sent to pyreadline3.


## Use:


#### To use this version of pyreadline3:

uninstall the old version:
```shell
pip uninstall pyreadline3
```

install this version:
```shell
pip install git+https://github.com/jplusc/pyreadline3.git
```


#### missing git for windows?
```shell
choco upgrade git -y
```

#### missing choco?
Seriously, if you have to use windows, use a package manager to make it less painfull. https://chocolatey.org/

from powershell:
```shell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```



### Some search keywords to lead others having trouble here:

`make_KeyPress_from_keydescr`
`Not a valid key: '%s'" % keydescr)`
`Not a valid key: '\e[d'`
`Not a valid key: '\e[c'`
`module 'collections' has no attribute 'Callable'`








## original readme below:
---

# pyreadline3

[![PyPi Badge](https://img.shields.io/pypi/v/pyreadline3)](https://pypi.org/project/pyreadline3/) 
![Publish](https://github.com/pyreadline3/pyreadline3/workflows/Publish/badge.svg)
![Test](https://github.com/pyreadline3/pyreadline3/workflows/Test/badge.svg)
[![Downloads](https://static.pepy.tech/personalized-badge/pyreadline3?period=week&units=international_system&left_color=black&right_color=orange&left_text=Last%20Week)](https://pepy.tech/project/pyreadline3)
[![Downloads](https://static.pepy.tech/personalized-badge/pyreadline3?period=month&units=international_system&left_color=black&right_color=orange&left_text=Month)](https://pepy.tech/project/pyreadline3)
[![Downloads](https://static.pepy.tech/personalized-badge/pyreadline3?period=total&units=international_system&left_color=black&right_color=orange&left_text=Total)](https://pepy.tech/project/pyreadline3)

The `pyreadline3` package is based on the stale package `pyreadline` located
[here](https://github.com/pyreadline/pyreadline).
The original `pyreadline` package is a python implementation of GNU `readline`
functionality.
It is based on the `ctypes` based UNC `readline` package by Gary Bishop.
It is not complete.
It has been tested for use with Windows 10.

Version 3.4+ of pyreadline3 runs on Python 3.5+.

`pyreadline3` is available on PyPI and can be installed with
```shell
pip install pyreadline3
```

## Features

- keyboard text selection and copy/paste
- Shift-arrowkeys for text selection
- Control-c can be used for copy activate with allow_ctrl_c(True) in config file
- Double tapping ctrl-c will raise a KeyboardInterrupt, use ctrl_c_tap_time_interval(x)
- where x is your preferred tap time window, default 0.3 s.
- paste pastes first line of content on clipboard.
- ipython_paste, pastes tab-separated data as list of lists or numpy array if all data is numeric
- paste_mulitline_code pastes multi line code, removing any empty lines.

The latest development version is always available at the project git
[repository](https://github.com/pyreadline3/pyreadline3)
