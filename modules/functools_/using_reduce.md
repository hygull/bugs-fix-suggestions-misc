# functools & operator


```python
In [54]: from functools import reduce                                                                                  

In [55]: l = [12, 56, 78, 34, 2, 2, 5, 89, 12, 56, 34, 23, 45, 0, 2]                                                   

In [56]: reduce(lambda a, b: a + b, l)                                                                                 
Out[56]: 450

In [57]: sum(l)                                                                                                        
Out[57]: 450

In [58]: # Max element                                                                                                 

In [59]: reduce(lambda a, b: a if a > b else b, l)                                                                     
Out[59]: 89

In [60]: max(l)                                                                                                        
Out[60]: 89
```


```python

In [61]: import operator # to use operator functions                                                                   

In [64]: reduce(operator.add, l)                                                                                       
Out[64]: 450


```


