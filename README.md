# ![PyQ](docs/img/pyq.png) PyQ – Python for kdb+

[![PyPI Version](https://img.shields.io/pypi/v/pyq.svg)](https://pypi.python.org/pypi/pyq)
![Build](https://github.com/KxSystems/pyq/workflows/Build/badge.svg?branch=master)
[![Windows build status](https://ci.appveyor.com/api/projects/status/ejiwxrll523smdca?svg=true)](https://ci.appveyor.com/project/abalkin/pyq)

[![Total alerts](https://img.shields.io/lgtm/alerts/g/KxSystems/pyq.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/KxSystems/pyq/alerts/)
[![Language grade: Python](https://img.shields.io/lgtm/grade/python/g/KxSystems/pyq.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/KxSystems/pyq/context:python)
[![Language grade: C/C++](https://img.shields.io/lgtm/grade/cpp/g/KxSystems/pyq.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/KxSystems/pyq/context:cpp)
[![Codecov](https://codecov.io/gh/KxSystems/pyq/branch/master/graph/badge.svg)](https://codecov.io/gh/KxSystems/pyq)

[PyQ](docs/README.md) brings the [Python programming language](https://www.python.org/about) to the [kdb+ database](https://kx.com).
Part of the [_Fusion for kdb+_](https://code.kx.com/q/interfaces/) interface collection.

It allows developers to integrate Python and q codes seamlessly in one application.
This is achieved by bringing the Python and q interpreters into the same process so that code written in either of the languages operates on the same data.
In PyQ, Python and q objects live in the same memory space and share the same
data.

Please [report issues](https://github.com/KxSystems/pyq/issues) in this repository.


## Installation

```bash
pip install pyq
```

See detailed [installation instructions](docs/install.md).

## Usage

For Python programmers:

```bash
pyq
```
```python
>>> from pyq import q
>>> 1 + q.til(10)
k('1 2 3 4 5 6 7 8 9 10')
```

or run your Python script as

```bash
pyq [python options] python-script
```

For q programmers:

```bash
q
```
```q
q)p)from math import hypot  / prefix python code with p)
q)p)q.h = hypot             / import a python function
q)h 3 4                     / call the python function from q
5f
```

## Documentation

:open_file_folder: [`docs`](docs/README.md)

## Testing

Use [tox](https://tox.readthedocs.io/en/latest) to run tests.

```bash
cd path/to/pyq/source
tox
```

