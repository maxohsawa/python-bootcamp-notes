# List Comprehensions

```
mystring = 'hello'
mylist = []

for letter in mystring:
	mylist.append(letter)
mylist
# ['h','e','l','l','o']
```

```
mystring = 'hello'
mylist = [letter for letter in mystring]
```

```
mylist = [x for x in 'word']
# ['w','o','r','d']
```

```
mylist = [x**2 for x in range(0,11)]
# [0,1,4,9,16,25,36,49,64,81,100]
```

```
mylist = [x**2 for x in range(0,11) if x%2==0]
# [0,4,16,36,64,100]
```

```
celsius = [0,10,20,34.5]
fahrenheit = [((9/5)*temp+32) for temp in celsius]
# [32.0, 50.0, 68.0, 94.1]
```

```
results = [x if x%2==0 else 'ODD' for x in range(0,11)]
# [0,'ODD',2,'ODD',4,'ODD',6,'ODD',8,'ODD',10]
```

```
mylist = [x*y for x in [2,4,6] for y in [1,10,1000]]
# [2,20,2000,4,40,4000,6,60,6000]
```