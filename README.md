# cx_Freeze 5.0 for Python 3.5 on Windows

This repository used to provide binary Python Wheels of cx_Freeze 5.0 for Python 3.5 on Windows.
However, on 2016-11-16 cx_Freeze 5.0 was finally declared stable and official binary Wheels
for multiple Python versions (including 3.5) [were uploaded to PyPI](https://pypi.python.org/pypi/cx_Freeze).
Since my binary packages of development snapshots have become obsolete, I have removed them from
this repository and you should use the official release from PyPI instead.

However, I will keep the previous build instructions here for a while:

## Build instructions

Python 3.5 is built with Visual Studio 2015, so you need to install it to compile extensions
for Python 3.5. The free [Community Edition](https://www.visualstudio.com/products/free-developer-offers-vs)
works without any problems - but you need to make sure that, for 64 bit platforms, you install the
'Common Tools for Visual C++ 2015' option, which is not included in the default installation.

Once Visual Studio 2015 is installed, building the cx_Freeze Wheel is very easy:

1. Open the *MSBuild Command Prompt for VS2015*.
2. Install the Wheel package with `pip install wheel`.
3. Either clone the cx_Freeze repository or download a
   [snapshot of the lastest version](https://bitbucket.org/anthony_tuininga/cx_freeze/downloads).
4. Build the Wheel with `python setup.py bdist_wheel`. You'll find the result in the `dist`
   directory.
5. Now you can install the created (or downloaded) Wheel with
   `pip install cx_Freeze-5.0-cp35-cp35m-win_amd64.whl` (for the 64 bit version). Make sure that
   your `pip` is a reasonably recent version because old `pip` versions can't install directly from
   wheels.
