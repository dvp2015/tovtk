[![Build Status](https://travis-ci.org/inr-kit/tovtk.svg?branch=master)](https://travis-ci.org/inr-kit/tovtk)

# tovtk
Python meshtal -> VTK converter.

Processes rectangular meshtallies. Output vtk files contain a rectilinear grid with cell values.

## Limitations
Only rectangular meshtally. 

In case `emesh` is used to split into energy bins, the resulting vtk file
contains values only from the total bin.

## Invocation

```bash
# Using the wrapper script:
>tovtk meshtal
# Using Python directly:
>pyhton -m tovtk meshtal
```

## Installation
Get source from the github:
```bash
>mkdir tovtk-git
>cd tovtk-git
>git clone git@github.com:inr-kit/tovtk.git .
```
Use [`pip`](https://pip.pypa.io/en/stable/) to install:
```bash
# with --user option does not require admin rights, 
# but PATH variable may need adjustments to point to 
# $HOME/.local/bin
>pip install --user -e .
# Or without the --user option. in this case requires admin rights
>sudo pip install -e .
```
If `pip` is not available in the system, it can be installed with the following commands:

```bash
# Download pip distribution, see https://pip.pypa.io/en/stable/installing/
>wget https://bootstrap.pypa.io/get-pip.py
# To install locally:
>python get-pip.py --user
# To install system-wide:
>sudo python get-pip.py
```
The local variant installs `pip` to `$HOME/.local/bin`. Ensure to add this folder to the `$PATH` variable.

## Dependensies
The tovtk package uses the numpy package and Python bindings to VTK library. In
a recent ubuntu they can be installed with 
```bash
>sudo apt-get install python-numpy
>sudo apt-get install python-vtk
```

Alternatively, [Anaconda](https://www.continuum.io) includes numpy and vtk among many others.

## Under windows
The current version of Python 2.7 is shipped with `pip`, which can be used to install the precompiled `numpy` package. 

