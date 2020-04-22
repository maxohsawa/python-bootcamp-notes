# modules and packages

```
pip install requests
```

```
pip install colorama

python

from colorama import init
init()
from colorama import FORE
print(Fore.GREEN + 'some green text')
```

```
pip install openpyxl
```

## pypi

python package index for finding packages

## using external module

in module file: mymodule.py
```
def my_func():
	print('Hey I am in mymodule.py')
```

in program file: myprogram.py
```
from mymodule import my_func

my_func()
# 'Hey I am in mymodule.py'
```

## creating package of modules

create empty __init__.py file in each directory and subdirectory

create script in main directory, MyMainPackage: some_main_script.py
```
def report_main():
	print('Hey I am in some_main_script.py in main package')
```

create script in subdirectory, SubPackage: mysubscript.py
```
def sub_report():
	print('Hey I am a function inside mysubscript.py')
```

in myprogram.py:
```
from MyMainPackage import some_main_script
from MyMainPackage.SubPackage import mysubscript

some_main_script.report_main()
# 'Hey I am in some_main_script.py in main package'

mysubscript.sub_report()
# 'Hey I am a function inside mysubscript.py'
```

to import specific function in module:
```

```

## __name__ and __main__

main() is implicit in python
```
__name__ == "__main__"
# this assignment occurs invisibly
```

in file one.py:
```
def func():
	print('func() in one.py')

print('top level in one.py')

if __name__ == '__main__':
	print('one.py is being run directly')
else:
	print('one.py has been imported')
```

in file two.py:
```
import one

print('top level in two.py')

one.func()

if __name__ == '__main__':
	print('two.py is being run directly')
else:
	print('two.py has been imported')
```

in command line:
```
python one.py
# 'top level in one.py'
# 'one.py is being run directly'
```

```
python two.py
# 'top level in one.py'
# 'one.py has been imported'
# 'top level in two.py'
# 'func() in one.py'
# 'two.py is being run directly'
```