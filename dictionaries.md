# dictionaries

```
d = {'key1':'value1','key2':'value2'}
# key-based, not index-based

d['key1']
# 'value1'

d['key3'] = 'value3'
# d = {'key1':'value1','key2':'value2','key3:'value3'}

d['key1'] = 'new_value'
# d = {'key1':'new_value','key2':'value2','key3:'value3'}
```

## keys(), values(), items()

```
d = {'key1':'value1','key2':'value2'}

d.keys()
# dict_keys(['key1','key2'])

d.values()
# dict_values(['value1,value2'])

d.items()
# dict_items([('key1','value1'),('key2','value2')])
# tuples
```
