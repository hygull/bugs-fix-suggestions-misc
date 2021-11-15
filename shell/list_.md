```python
In [1]: l = [1, 3, 7]                                                                                                  

In [2]: l2 = list()                                                                                                    

In [3]: l2.append(8)                                                                                                   

In [4]: l2.append(5)                                                                                                   

In [5]: l                                                                                                              
Out[5]: [1, 3, 7]

In [6]: l2                                                                                                             
Out[6]: [8, 5]

In [7]:                                                                                                                

```


```python
In [7]: l2.pop(0)                                                                                                      
Out[7]: 8

In [8]: l2.pop()                                                                                                       
Out[8]: 5

In [9]: l3 = range(10)                                                                                                 

In [10]: l3                                                                                                            
Out[10]: range(0, 10)

In [11]: l3 = list(l3)                                                                                                 

In [12]: l3                                                                                                            
Out[12]: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

In [13]: l3.pop()                                                                                                      
Out[13]: 9

In [14]: l3                                                                                                            
Out[14]: [0, 1, 2, 3, 4, 5, 6, 7, 8]

In [15]: l3.remove(0)                                                                                                  

In [16]: l3                                                                                                            
Out[16]: [1, 2, 3, 4, 5, 6, 7, 8]
```