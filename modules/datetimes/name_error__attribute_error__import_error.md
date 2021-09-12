## NameError

```python
In [1]: from datetime import datetime, date, strftime, strptime                                                        
---------------------------------------------------------------------------
ImportError                               Traceback (most recent call last)
<ipython-input-1-2cc4de47884f> in <module>
----> 1 from datetime import datetime, date, strftime, strptime

ImportError: cannot import name 'strftime'

In [2]: from datetime import datetime, date, strptime                                                                  
---------------------------------------------------------------------------
ImportError                               Traceback (most recent call last)
<ipython-input-2-3b05bf80e285> in <module>
----> 1 from datetime import datetime, date, strptime

ImportError: cannot import name 'strptime'

In [3]: from datetime import datetime, date                                                                            

In [4]: start = datetime.now()                                                                                         

In [5]: end = datetime.now()                                                                                           

In [6]: end - start                                                                                                    
Out[6]: datetime.timedelta(0, 11, 194854)

In [7]: diff = (end - start) 
```

## AttributeError

```python

In [8]: diff.hour                                                                                                      
---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-8-362d777f512b> in <module>
----> 1 diff.hour

AttributeError: 'datetime.timedelta' object has no attribute 'hour'

In [9]: dir(diff)                                                                                                      
Out[9]: 
['__abs__',
 '__add__',
 '__bool__',
 '__class__',
 '__delattr__',
 '__dir__',
 '__divmod__',
 '__doc__',
 '__eq__',
 '__floordiv__',
 '__format__',
 '__ge__',
 '__getattribute__',
 '__gt__',
 '__hash__',
 '__init__',
 '__init_subclass__',
 '__le__',
 '__lt__',
 '__mod__',
 '__mul__',
 '__ne__',
 '__neg__',
 '__new__',
 '__pos__',
 '__radd__',
 '__rdivmod__',
 '__reduce__',
 '__reduce_ex__',
 '__repr__',
 '__rfloordiv__',
 '__rmod__',
 '__rmul__',
 '__rsub__',
 '__rtruediv__',
 '__setattr__',
 '__sizeof__',
 '__str__',
 '__sub__',
 '__subclasshook__',
 '__truediv__',
 'days',
 'max',
 'microseconds',
 'min',
 'resolution',
 'seconds',
 'total_seconds']

In [10]: diff.days                                                                                                     
Out[10]: 0

In [11]: diff.seconds                                                                                                  
Out[11]: 11

In [12]: diff.total_seconds                                                                                            
Out[12]: <function timedelta.total_seconds>

In [13]: diff.total_seconds()                                                                                          
Out[13]: 11.194854

In [14]: diff.max                                                                                                      
Out[14]: datetime.timedelta(999999999, 86399, 999999)

In [15]: diff.min                                                                                                      
Out[15]: datetime.timedelta(-999999999)

In [16]: diff.resolution                                                                                               
Out[16]: datetime.timedelta(0, 0, 1)

In [17]: diff.resolution.__str__                                                                                       
Out[17]: <method-wrapper '__str__' of datetime.timedelta object at 0x10a162d78>

In [18]: diff.resolution.__str__()                                                                                     
Out[18]: '0:00:00.000001'

```

## NameError

```python

In [19]: dff.microseconds                                                                                              
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-19-254ce219d9b1> in <module>
----> 1 dff.microseconds

NameError: name 'dff' is not defined

In [20]: diff.microseconds                                                                                             
Out[20]: 194854

In [21]: help(diff.resolution)                                                                                         


In [22]:  
```       

