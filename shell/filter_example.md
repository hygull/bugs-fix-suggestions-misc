```python
In [59]: l                                                                                                             
Out[59]: [1, 4, 5, 6, 7]

In [60]: filter(lambda n: n % 2 == 0, l)                                                                               
Out[60]: <filter at 0x11cb53a90>

In [61]: list(filter(lambda n: n % 2 == 0, l))                                                                         
Out[61]: [4, 6]

In [62]:                                                                                                               
```