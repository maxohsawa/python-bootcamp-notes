# lambda expressions, map, and filter

## maps

```
def square(num):
	return num**2

my_nums = [1,2,3,4,5]

for item in map(square,my_nums):
	print(item)
# prints squares

list(map(square,my_nums))
# [1,4,9,16,25]
```

```
def splicer(mystring):
	if len(mystring)%2 == 0:
		return 'EVEN'
	else:
		return mystring[0]

names = ['Andy','Eve','Sally']
list(map(splicer,names))
# ['EVEN','E','S']
```

## filters

```
def check_even(num):
	return num%2==0

mynums = [1,2,3,4,5,6]

list(filter(check_even,mynums))
# [2,4,6]
```

## lambda expressions

### lambda map

```
def square(num):
	result = num**2
	return result

# can be written as

def square(num): return num ** 2

# can be written as

square = lambda num: num**2

mynums = [1,2,3,4,5]

list(map(lambda num:num**2, mynums))

# [1,4,9,16,25]
```

### lambda filter

```
mynums = [1,2,3,4,5,6]

list(filter(lambda num:num%2==0,mynums))

# [2,4,6]
```