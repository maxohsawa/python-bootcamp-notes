# args and kwargs

```
def myfunc(*args, **kwargs):
	print('I would like {} {}'.format(args[0],kwargs['food']))
```

```
my func(10,20,30,fruit='orange',food='eggs',animal='dog')
# 'I would like 10 eggs'
```