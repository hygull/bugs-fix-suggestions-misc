# Dict 

```python
In [46]: d4 = {*d, **d2}                                                                                               
  File "<ipython-input-46-ccb3a9b5ff0d>", line 1
    d4 = {*d, **d2}
               ^
SyntaxError: invalid syntax
```


```python
In [36]: d = dict(a=1, b=2, c=3, d=4)                                                                                  

In [37]: d                                                                                                             
Out[37]: {'a': 1, 'b': 2, 'c': 3, 'd': 4}

In [38]: d2 = dict(p=12, q=23, r=45, s=56, t=89)                                                                       

In [39]: d2                                                                                                            
Out[39]: {'p': 12, 'q': 23, 'r': 45, 's': 56, 't': 89}
```

# ChainMap Example

```python
In [42]: d3 = ChainMap.map(d, d2)                                                                                      
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-42-03673a3ecefe> in <module>
----> 1 d3 = ChainMap.map(d, d2)

AttributeError: type object 'ChainMap' has no attribute 'map'
```

```python
In [41]: from collections import ChainMap                                                                              

In [43]: d3 = ChainMap(d, d2)                                                                                          

In [44]: d3                                                                                                            
Out[44]: ChainMap({'a': 1, 'b': 2, 'c': 3, 'd': 4}, {'p': 12, 'q': 23, 'r': 45, 's': 56, 't': 89})

In [45]: dict(d3)                                                                                                      
Out[45]: {'d': 4, 's': 56, 'r': 45, 'q': 23, 't': 89, 'a': 1, 'b': 2, 'c': 3, 'p': 12}

In [47]: d4 = {**d, **d2}                                                                                              

In [48]: d4                                                                                                            
Out[48]: {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'p': 12, 'q': 23, 'r': 45, 's': 56, 't': 89}

In [49]: d4 = {**d2, **d}                                                                                              

In [50]: d4                                                                                                            
Out[50]: {'p': 12, 'q': 23, 'r': 45, 's': 56, 't': 89, 'a': 1, 'b': 2, 'c': 3, 'd': 4}

In [51]: d.update(d2)                                                                                                  

In [52]: d                                                                                                             
Out[52]: {'a': 1, 'b': 2, 'c': 3, 'd': 4, 'p': 12, 'q': 23, 'r': 45, 's': 56, 't': 89}

```