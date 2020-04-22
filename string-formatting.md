# string formatting

## upper() and lower()

```
x = 'Hello World'
x.upper()
# 'HELLO WORLD'
# .lower()
```

## split()

```
x = 'Hello World'
x.split()
# ['Hello', 'World']
# defaults to whitespace
```

## join()

```
mylist = ['Hello','World']
print(' '.join(mylist))
# 'Hello World'
```

# print formatting

## format()

```
'I am free on {} and {}'.format('Monday', 'Wednesday')
# 'I am free on Monday and Wednesday'
```

```
'The {2} {1} {0}'.format('fox','brown','quick')
# 'The quick brown fox'
```

```
'The {q} {b} {f}'.format(f='fox',b='brown',q='quick')
# 'The quick brown fox'
```

## f string literal

```
name = 'Jose'
f'Hello, his name is {name}'
# 'Hello, his name is Jose'