```python
In [14]: df = pd.DataFrame([(1,3,5, 7, 9), (12, 45, 67, 88, 90), (14, 68, 90, 32, 54)], columns=['set1', 'set2', 'set3', 'set4', 'set5'])      

In [15]: df                                                                                                                                    
Out[15]: 
   set1  set2  set3  set4  set5
0     1     3     5     7     9
1    12    45    67    88    90
2    14    68    90    32    54

In [16]: df['set1']                                                                                                                            
Out[16]: 
0     1
1    12
2    14
Name: set1, dtype: int64

In [17]: df['set1'][0]                                                                                                                         
Out[17]: 1

In [18]: df['set1'][2]                                                                                                                         
Out[18]: 14

In [19]:                                                                                                                                       
```

```python
In [19]: df = pd.DataFrame({'set1': [23, 45, 6, 78, 89], 'set2': [43, 32, 21, 90, 45], 'set3': [89, 45, 32, 9, 8]})                            

In [20]: df                                                                                                                                    
Out[20]: 
   set1  set2  set3
0    23    43    89
1    45    32    45
2     6    21    32
3    78    90     9
4    89    45     8

In [21]: df[df.set1 > 70]                                                                                                                      
Out[21]: 
   set1  set2  set3
3    78    90     9
4    89    45     8

In [22]: df[df.set3 < 10]                                                                                                                      
Out[22]: 
   set1  set2  set3
3    78    90     9
4    89    45     8

In [23]: df[df.set3 > 10]                                                                                                                      
Out[23]: 
   set1  set2  set3
0    23    43    89
1    45    32    45
2     6    21    32

In [24]: df[df.set3 == 10]                                                                                                                     
Out[24]: 
Empty DataFrame
Columns: [set1, set2, set3]
Index: []

In [25]: df[df.set3 == 32]                                                                                                                     
Out[25]: 
   set1  set2  set3
2     6    21    32

In [26]:        

```