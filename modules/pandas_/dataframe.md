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


```python
In [26]: column1 = pd.Series([1, 45, 67, 89, 90])                                                                                              

In [27]: column2 = pd.Series([11, 50, 60, 30, 9])                                                                                              

In [28]: column3 = pd.Series([89, 23, 65, 33, 39])                                                                                             

In [29]: df = pd.DataFrame()                                                                                                                   

In [30]: df.set1 = column1                                                                                                                     
/Library/Frameworks/Python.framework/Versions/3.6/bin/ipython:1: UserWarning: Pandas doesn't allow columns to be created via a new attribute name - see https://pandas.pydata.org/pandas-docs/stable/indexing.html#attribute-access
  #!/Library/Frameworks/Python.framework/Versions/3.6/bin/python3.6

In [31]: df                                                                                                                                    
Out[31]: 
Empty DataFrame
Columns: []
Index: []

In [32]: df["set1"] = column1                                                                                                                  

In [33]: df                                                                                                                                    
Out[33]: 
   set1
0     1
1    45
2    67
3    89
4    90

In [34]: df["set2"] = column2                                                                                                                  

In [35]: df["set3"] = column3                                                                                                                  

In [36]: df                                                                                                                                    
Out[36]: 
   set1  set2  set3
0     1    11    89
1    45    50    23
2    67    60    65
3    89    30    33
4    90     9    39

In [37]: df.set1                                                                                                                               
Out[37]: 
0     1
1    45
2    67
3    89
4    90
dtype: int64

In [38]: df['set1']                                                                                                                            
Out[38]: 
0     1
1    45
2    67
3    89
4    90
Name: set1, dtype: int64

In [39]:     
```