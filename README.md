# **Advisory**

**This library is an experimental project porting the original PyMISP project to python async to address I/O bound processing difficulties often encountered when using large MISP instances.**

**It is an ALPHA release, this code has not been tested, USE AT YOUR OWN RISK!**

# PyMISP - Python Library to access MISP

PyMISP is a Python library to access [MISP](https://github.com/MISP/MISP) platforms via their REST API.

PyMISP allows you to fetch events, add or update events/attributes, add or update samples or search for attributes.

This project aims at porting the original PyMISP project to Python async using the `aiohttp` library instead of the synchronous `requests` library.

## Install from pip

**It is strongly recommended to use a virtual environment**

If you want to know more about virtual environments, [python has you covered](https://docs.python.org/3/tutorial/venv.html)

Only basic dependencies:
```
pip3 install pymisp-async
```

## Install the latest version from repo from development purposes

**Note**: poetry is required; e.g., "pip3 install poetry"

```
git clone https://github.com/pixmaip/PyMISP-async.git && cd PyMISP-async
git submodule update --init
poetry install
```

## Usage

Initialize the `PyMISP` object using the asynchronous context manager:
```
async with PyMISP(url, key) as misp_obj:
    events = await misp_obj.events()
```

## Documentation

The official MISP documentation is available [here](https://pymisp.readthedocs.io/en/latest/).

All `async` functions present in this library use the same API as the original MISP package.

# License

PyMISP is distributed under an [open source license](./LICENSE). A simplified 2-BSD license.

