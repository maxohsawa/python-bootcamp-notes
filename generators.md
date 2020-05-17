# generators

## example of problem

```
def create_cubes(n):
	result = []
	for x in range(n):
		result.append(x**3)
	return result
```
this creates a large list in memory when we only need elements one at a time

## use yield keyword for memory efficiency

this yields values as necessary

```
def create_cubes(n):
	
	for x in range(n):
		yield x**3
```

range() is a generator so you cannot access it as a list without casting it

```
list(create_cubes(10))

# [0,1,8,27,64,125,216,343,512,729]
```

## fibonacci example

```
def gen_fibonacci(n):
	
	a = 1
	b = 1
	for i in range(n):
		yield a
		a,b = b,a+b

for number in gen_fibonacci(10):
	print(number)
```

## next

```
def simple_gen():
	for x in range(3):
		yield x

for number in simple_gen():
	print(number)

# 0
# 1
# 2

g = simple_gen()

print(next(g))
# 0

print(next(g))
# 1

print(next(g))
# 2

print(next(g))
# StopIteration Error
```

## iter

```
s = 'hello'

for letter in s:
	print(letter)

# h
# e
# l
# l
# o

next(s)

# TypeError sting s is not an interator

s_iter = iter(s)

next(s_iter)
# h

next(s_iter)
# e
```