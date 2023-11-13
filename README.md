---
title: ssh-python
---

Bindings for [libssh](https://www.libssh.org) C library.

[![License](https://img.shields.io/badge/License-LGPL%20v2-blue.svg)](https://pypi.python.org/pypi/ssh-python)

[![Latest Version](https://img.shields.io/pypi/v/ssh-python.svg)](https://pypi.python.org/pypi/ssh-python)

[![image](https://circleci.com/gh/ParallelSSH/ssh-python/tree/master.svg?style=shield)](https://circleci.com/gh/ParallelSSH/ssh-python/tree/master)

[![image](https://img.shields.io/pypi/wheel/ssh-python.svg)](https://pypi.python.org/pypi/ssh-python)

[![image](https://img.shields.io/pypi/pyversions/ssh-python.svg)](https://pypi.python.org/pypi/ssh-python)

[![image](https://ci.appveyor.com/api/projects/status/2t4bmmtjvfy5s1in/branch/master?svg=true)](https://ci.appveyor.com/project/pkittenis/ssh-python)

[![Latest documentation](https://readthedocs.org/projects/ssh-python/badge/?version=latest)](http://ssh-python.readthedocs.org/en/latest/)

# Installation

Binary wheels are provided for Linux (manylinux 2010), OSX (10.14 and
10.15 for brew Python), and Windows 64-bit (Python 3.6/3.7/3.8).

Wheels have *no dependencies*.

For building from source, see
[documentation](https://ssh-python.readthedocs.io/en/latest/installation.html#building-from-source).

``` shell
pip install ssh-python
```

Pip may need to be updated to be able to install binary wheels.

``` shell
pip install -U pip
pip install ssh-python
```

# Quick Start

See [command execution
script](https://github.com/ParallelSSH/ssh-python/blob/master/examples/exec.py)
for complete example.

# Features

The library uses [Cython](https://www.cython.org) based native code
extensions as wrappers to `libssh`.

-   Thread safe - GIL released as much as possible
    -   libssh threading limitations apply - anything not supported in C
        is not supported in Python
-   Very low overhead thin wrapper
-   Object oriented
    -   Memory freed automatically and safely as objects are garbage
        collected by Python
-   Uses Python semantics where applicable
    -   channel/file handle context manager support
    -   channel/file handle iterator support
-   Raises low level C errors as Python exceptions
