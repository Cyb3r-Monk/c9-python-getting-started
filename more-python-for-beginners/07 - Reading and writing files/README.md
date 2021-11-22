# Working with files

Python allows you to read and write from files. [io](https://docs.python.org/3/library/io.html) is the module that provides Python capabilities for input/output (I/O), including text I/O from files

## Microsoft Learn Resources

Explore related tutorials on [Microsoft Learn](https://learn.microsoft.com/?WT.mc_id=python-c9-niner)

## Modes:
`r` - Read (default)  
`w` - Truncate and write  
`a` - Append if file exists  
`x` - Write, fail if file exists  
`+` - Updating (read/write)  

`t` - Text (default)  
`b` - Binary  

## Using with
`with` automatically closes resources. No need to manually close the file after using it. 

```python
with open('output.txt', 'wt') as stream:
    stream.write('Lorem ipsum dolar')
```