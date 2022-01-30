# Tuple

```python
In [81]: t = (1,)                                                                                                      

In [82]: type(t)                                                                                                       
Out[82]: tuple

In [83]: t2 = (12, 45, 6)                                                                                              

In [84]: t + t2                                                                                                        
Out[84]: (1, 12, 45, 6)

In [87]: t3 = tuple({1: 45, 67: 89, 23: 12})                                                                           

In [88]: t3                                                                                                            
Out[88]: (1, 67, 23)

In [89]:  

```


```python
In [89]: t4 = tuple()                                                                                                  

In [90]: t4                                                                                                            
Out[90]: ()

In [91]: t5 = tuple(pd.Series([1, 5, 89, 90]))                                                                         

In [92]: t5                                                                                                            
Out[92]: (1, 5, 89, 90)

In [93]: df = pd.DataFrame()                                                                                           

In [94]: df['col1'] = pd.Series([1, 5, 89, 90])                                                                        

In [95]: df                                                                                                            
Out[95]: 
   col1
0     1
1     5
2    89
3    90

In [96]: df.shape                                                                                                      
Out[96]: (4, 1)

In [98]: df.shape[0] # -> no. of cols                                                                                  
Out[98]: 4

```

```python
In [115]: np.array([12, 45, 67])                                                                                       
Out[115]: array([12, 45, 67])

In [116]: arr = np.array([12, 45, 67])                                                                                 

In [117]: arr + 10                                                                                                     
Out[117]: array([22, 55, 77])

In [118]: arr2 = np.array((23, 45, 67))                                                                                

In [119]: arr3 = arr + arr2                                                                                            

In [120]: arr3                                                                                                         
Out[120]: array([ 35,  90, 134])
```