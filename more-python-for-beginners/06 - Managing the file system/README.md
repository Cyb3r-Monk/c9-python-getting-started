# Managing the file system

Python's [pathlib](https://docs.python.org/3/library/pathlib.html) provides operations and classes to access files and directories in the file system.

## Microsoft Learn Resources

Explore related tutorials on [Microsoft Learn](https://learn.microsoft.com/?WT.mc_id=python-c9-niner)

## Working with Paths

```python
# Python 3.6 or higher
# Grab the library
from pathlib import Path

# What is the current working directory?
cwd = Path.cwd()
print('\nCurrent working directory:\n' + str(cwd))

# Create full path name by joining path and filename
new_file = Path.joinpath(cwd, 'new_file.txt')
print('\nFull path:\n' + str(new_file))

# Check if file exists
print('\nDoes that file exist? ' + str(new_file.exists()) + '\n')
```

## Working with directories

```python
from pathlib import Path
cwd = Path.cwd()

# Get the parent directory
parent = cwd.parent

# Is this a directory?
print('\nIs this a directory? ' + str(parent.is_dir()))

# Is this a file?
print('\nIs this a file? ' + str(parent.is_file()))

# List child directories
print('\n-----directory contents-----')
for child in parent.iterdir():
    if child.is_dir():
        print(child)

```

## Working with Files

```python
from pathlib import Path
cwd = Path.cwd()

demo_file = Path(Path.joinpath(cwd, 'demo.txt'))

# Get the file name
print('\nfile name: ' + demo_file.name)

# Get the extension
print('\nfile suffix: ' + demo_file.suffix)

# Get the folder
print('\nfile folder: ' + demo_file.parent.name)

# Get the size
print('\nfile size: ' + str(demo_file.stat().st_size) + '\n')
```