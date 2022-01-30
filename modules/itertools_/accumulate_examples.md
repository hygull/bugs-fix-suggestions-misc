# accumulate examples


```python
In [121]: from itertools import accumulate                                                                             

In [122]: nums = [12, 45, 67, 89]                                                                                      

In [123]: _sum = accumulate(nums, lambda num1, num2: num1 + num2)                                                      

In [124]: _sum                                                                                                         
Out[124]: <itertools.accumulate at 0x10d2b11c8>

In [125]: list(_sum)                                                                                                   
Out[125]: [12, 57, 124, 213]
```

```python
In [126]: list(_sum)[0]                                                                                                
---------------------------------------------------------------------------
IndexError                                Traceback (most recent call last)
<ipython-input-126-59685a861059> in <module>
----> 1 list(_sum)[0]

IndexError: list index out of range
```

```python
In [127]: _sum                                                                                                         
Out[127]: <itertools.accumulate at 0x10d2b11c8>

In [128]: next(_sum)                                                                                                   
---------------------------------------------------------------------------
StopIteration                             Traceback (most recent call last)
<ipython-input-128-7539e7e8cdf1> in <module>
----> 1 next(_sum)

StopIteration: 

```

```python
In [129]: _sum = accumulate(nums, lambda num1, num2: num1 + num2)                                                      

In [130]: list(_sum)[0]                                                                                                
Out[130]: 12

In [131]: next(_sum)                                                                                                   
---------------------------------------------------------------------------
StopIteration                             Traceback (most recent call last)
<ipython-input-131-7539e7e8cdf1> in <module>
----> 1 next(_sum)

StopIteration: 
```

```python
In [132]: _sum = accumulate(nums, lambda num1, num2: num1 + num2)                                                      

In [133]: next(_sum)                                                                                                   
Out[133]: 12

In [134]: next(_sum)                                                                                                   
Out[134]: 57

In [135]: next(_sum)                                                                                                   
Out[135]: 124

In [136]: next(_sum)                                                                                                   
Out[136]: 213

In [137]: next(_sum)                                                                                                   
---------------------------------------------------------------------------
StopIteration                             Traceback (most recent call last)
<ipython-input-137-7539e7e8cdf1> in <module>
----> 1 next(_sum)

StopIteration: 

In [138]:       
```