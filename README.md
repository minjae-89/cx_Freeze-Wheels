# cx_Freeze 5.0 for Python 3.5 on Windows

As of April 2016 both [py2exe](http://www.py2exe.org/) and the current stable version of
[cx_Freeze](http://cx-freeze.sourceforge.net/) (4.3.4) don't have any support for Python 3.5.
However, the development version of cx_Freeze 5.0 from
[its Bitbucket repository](https://bitbucket.org/anthony_tuininga/cx_freeze) already has good
support for Python 3.5, but no binary packages are easily available.

This page aims to provide both pre-built Python Wheels (32 and 64 bit) of the cx_Freeze 5.0
development version and some simple instructions how to build the Python Wheels.

Python 3.5 is built with Visual Studio 2015, so you need to install it to compile extensions
for Python 3.5. The free [Community Edition](https://www.visualstudio.com/products/free-developer-offers-vs)
works without any problems.

Once Visual Studio 2015 is installed, building the cx_Freeze Wheel is very easy:

1. Open the *MSBuild Command Prompt for VS2015*.
2. Install the Wheel package with `pip install wheel`.
3. Either clone the cx_Freeze repository or download a
   [snapshot of the lastest version](https://bitbucket.org/anthony_tuininga/cx_freeze/downloads).
4. Build the Wheel with `python setup.py bdist_wheel`. You'll find the result in the `dist`
   directory.
5. Now you can install the created (or downloaded) Wheel with
   `pip install cx_Freeze-5.0-cp35-cp35m-win_amd64.whl` (for the 64 bit version).

The binary Wheels on this page are the repository version `a69936ec621c`
of cx_Freeze 5.0, built with Visual Studio Community 2015 Update 2 on 2016-04-08.