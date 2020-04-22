# useful operators

## range

```
#range(start, stop, step)
for num in range(3,10,2):
	print(num)
```

```
list(range(0,11,2))
```

## enumerate

```
for item in enumerate(word):
	print(item)
	#prints tuples
```

```
for index, letter in enumerate(word):
	print(index)
	print(letter)
	print('\n')
```

## zip

```
mylist1 = [1,2,3]
mylist2 = ['a','b','c']
for item in zip(mylist1, mylist2):
	print(item)
	#prints tuples
```
**zip** only zips up to the shortest list

## in

```
'x' in ['x', 'y', 'z']
True
```
```
a in 'a world'
True
```
```
d = {'mykey':345}
'mykey' in d
True
```
```
345 in d.values()
True
```

## min and max

```
mylist = [10, 20, 30, 40, 100]
min(mylist)
10
max(mylist)
100
```

## random

```
from random import shuffle
shuffle(my_list)
```
shuffles list **in place**

```
from random import randint
randint(0,100)
```

## input

```
result = input('What is your name?')
```

## type casting

```
float(result)
int(result)
result = int(input('How old are you?'))
```
