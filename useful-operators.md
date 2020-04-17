# Useful Operators



## "in"

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

## "random"

```
from random import shuffle
shuffle(my_list)
```
shuffles list **in place**

```
from random import randint
randint(0,100)
```