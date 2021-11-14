# Packages and modules

## Modules

[Modules](https://docs.python.org/3/tutorial/modules.html) allow you to store reusable blocks of code, such as functions, in separate files. They're referenced by using the `import` statement.

``` python
# import module as namespace
import helpers
helpers.display('Not a warning')

# import all into current namespace
from helpers import *
display('Not a warning')

# import specific items into current namespace
from helpers import display
display('Not a warning')
```

## Packages

[Distribution packages](https://packaging.python.org/glossary/#term-distribution-package) are external archive files which contain resources such as classes and functions. Most every application you create will make use of one or more packages. Imports from packages follow the same syntax as modules you've created. The [Python Package index](https://pypi.org/) contains a full list of packages you can install using [pip](https://pip.pypa.io/en/stable/).

```python
# Install an individual package
pip install colorama

# Install from a list of packages
pip install -r requirements.txt

# requirements.txt
colorama
```

## Virtual environments

[Virtual environments](https://docs.python.org/3.7/tutorial/venv.html) allow you to install packages into an isolated folder. This allows you to better manage versions.

By default, packages are installed globally. This makes version management of packages a challenge.

``` console
# Install virtual environment (globally)
pip install virtualenv

# create a virtual environment (Windows)
# python -m venv <folder_name>
python -m venv .venv
# Activate the virtual environment
# <folder_name>\Scripts\Activate.bat (or .ps1)
.venv\Scripts\Activate.ps1

# create a virtual environment (OSX/Linux)
virtualenv <folder_name>
# Activate the virtual environment
# <folder_name>/bin/activate
```

After activating the virtual environment, packages and modules can be installed in the virtual environment.