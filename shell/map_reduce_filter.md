```python
In [16]:                                                                                                                                       

In [16]: l = [1, 4, 6, 78, 8, 0, -1, 45]                                                                                                       

In [17]: l.sort()                                                                                                                              

In [18]: l                                                                                                                                     
Out[18]: [-1, 0, 1, 4, 6, 8, 45, 78]

In [19]: l2 = [1, 4, 6, 78, 8, 0, -1, 45]                                                                                                      

In [20]: sorted(l2)                                                                                                                            
Out[20]: [-1, 0, 1, 4, 6, 8, 45, 78]

In [21]: l2                                                                                                                                    
Out[21]: [1, 4, 6, 78, 8, 0, -1, 45]

In [22]: filter(lambda num: num % 2 == 0)                                                                                                      
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-22-90c5d5f3d463> in <module>
----> 1 filter(lambda num: num % 2 == 0)

TypeError: filter expected 2 arguments, got 1

In [23]: filter(lambda num: num % 2 == 0, l2)                                                                                                  
Out[23]: <filter at 0x11011fda0>

In [24]: list(filter(lambda num: num % 2 == 0, l2))                                                                                            
Out[24]: [4, 6, 78, 8, 0]

In [25]: reduce(lambda num1, num2: num1, num2, l2, 0)                                                                                          
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-25-a8c598d8c511> in <module>
----> 1 reduce(lambda num1, num2: num1, num2, l2, 0)

NameError: name 'reduce' is not defined

In [26]: from functools import reduce                                                                                                          

In [27]: reduce(lambda num1, num2: num1, num2, l2, 0)                                                                                          
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-27-a8c598d8c511> in <module>
----> 1 reduce(lambda num1, num2: num1, num2, l2, 0)

NameError: name 'num2' is not defined

In [28]: reduce(lambda num1, num2: num1 + num2, l2, 0)                                                                                         
Out[28]: 141

In [29]: sum(l2)                                                                                                                               
Out[29]: 141

In [30]: map(lambda num: num ** 2, l2)                                                                                                         
Out[30]: <map at 0x1101f2828>

In [31]: list(map(lambda num: num ** 2, l2))                                                                                                   
Out[31]: [1, 16, 36, 6084, 64, 0, 1, 2025]

In [32]:                   

```