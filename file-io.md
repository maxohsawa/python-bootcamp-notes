# file io

```
%%writefile myfile.txt
# %%writefil only works in jupyter
First line
second line
third line
```

## read() and seek()

```
myfile = open('myfile.txt')
myfile.read()
# returns giant string
myfile.seek(0)
# reset read point to beginning
```

## readlines()

```
myfile.readlines()
# returns list of strings corresponding to lines
```

## close()

files opened need to be closed
```
myfile.close()
```

## with open

files opened and copied to a variable like this don't need to be closed
```
with open('myfile.txt') as my_new_file:
	contents = my_new_file.read()
```

## write and read modes

read with mode='r'
```
with open('myfile.txt', mode='r') as myfile:
	contents = myfile.read()
```

write with mode='w' (will overwrite files or create new)
```
with open('myfile.txt',mode='w') as myfile:
	myfile.write('This is all that is in here')
```

append with mode='a'
```
with open('myfile.txt',mode='a') as myfile:
	myfile.write('This is the fourth line')
```

mode='r+' for reading and writing

mode='w+' for writing and reading (overwrites existing files or creates a new one)