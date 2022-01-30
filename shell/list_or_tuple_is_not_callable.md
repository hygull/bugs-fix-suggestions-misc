```python
In [99]: t                                                                                                             
Out[99]: (1,)

In [100]: t2                                                                                                           
Out[100]: (12, 45, 6)

In [101]: m = map(t, t2)                                                                                               

In [102]: m                                                                                                            
Out[102]: <map at 0x11970b550>
```

```python
In [103]: next(m)                                                                                                      
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-103-8efa10874b95> in <module>
----> 1 next(m)

TypeError: 'tuple' object is not callable

In [104]: for i in m: 
     ...:     print(i) 
     ...:                                                                                                              
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-104-9cd7b7f0b3b5> in <module>
----> 1 for i in m:
      2     print(i)
      3 

TypeError: 'tuple' object is not callable

```

```python
In [105]: list(m)                                                                                                      
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-105-444b761b1f09> in <module>
----> 1 list(m)

TypeError: 'tuple' object is not callable

In [106]: type(m)                                                                                                      
Out[106]: map

In [107]: m = map([12, 56], [12, 45])                                                                                  

In [108]: m                                                                                                            
Out[108]: <map at 0x11a26d6d8>

In [109]: list(m)                                                                                                      
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-109-444b761b1f09> in <module>
----> 1 list(m)

TypeError: 'list' object is not callable
```

```python
In [110]: map(lambda n: n ** 2, [12, 34])                                                                              
Out[110]: <map at 0x10bf580b8>

In [111]: list(map(lambda n: n ** 2, [12, 34]))                                                                        
Out[111]: [144, 1156]

In [112]:               
```