# string indexing and slicing

## index, negative indexing
```
mystring = 'Hello'

mystring[1]
# 'e'

mystring[-2]
# 'l'
```

## slicing
```
mystring = 'Hello'

new_string = mystring[1:]
# 'ello'

new_string = mystring[1:4]
# 'Hell'

new_string = mystring[::2]
# 'Hlo'

new_string = mystring[::-1]
# 'olleH'
