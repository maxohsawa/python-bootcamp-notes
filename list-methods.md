# list methods

## append

```
new_list = ['one', 'two', 'three', 'four']
new_list.append('five')
# ['one', 'two', 'three', 'four', 'five']
```

## pop

```
new_list = ['one', 'two', 'three', 'four']
num = new_list.pop()
# 'four'

new_list = ['one', 'two', 'three', 'four']
num = new_list.pop(0)
# 'one'
```

## sort

```
new_list = ['a','e','x','b','c']
num_list = [4,1,8,3]

new_list.sort()
# sorts in place
# ['a','b','c','e','x']

num_list.sort()
# [1,3,4,8]
```

## reverse

```
num_list = [4,1,8,3]
num_list.sort()
#[1,3,4,8]
num_list.reverse()
# reverses in place
# [8,4,3,1]