This I found as a best place to read -> [https://kanoki.org/2019/07/17/pandas-how-to-replace-values-based-on-conditions/](https://kanoki.org/2019/07/17/pandas-how-to-replace-values-based-on-conditions/)

```python
In [8]: df = pd.DataFrame({'a': [1, 4, 5, 6, 7], 'b': [45, 6,78, 90, 78], 'c': [45, 68, 90, 12, 34]})         

In [9]: df                                                                                                    
Out[9]: 
   a   b   c
0  1  45  45
1  4   6  68
2  5  78  90
3  6  90  12
4  7  78  34

In [10]: df2 = df.copy()                                                                                      

In [11]: df2                                                                                                  
Out[11]: 
   a   b   c
0  1  45  45
1  4   6  68
2  5  78  90
3  6  90  12
4  7  78  34

In [12]: df.loc[df['a'] == 1] = 10                                                                            

In [13]: df                                                                                                   
Out[13]: 
    a   b   c
0  10  10  10
1   4   6  68
2   5  78  90
3   6  90  12
4   7  78  34

```

```python

In [15]: df.loc[df['a'] == 1] = 10                                                                            

In [16]: df                                                                                                   
Out[16]: 
    a   b   c
0  10  10  10
1   4   6  68
2   5  78  90
3   6  90  12
4   7  78  34

In [17]: df.loc[df['b'] < 20, 'c'] = 55                                                                       

In [18]: df                                                                                                   
Out[18]: 
    a   b   c
0  10  10  55
1   4   6  55
2   5  78  90
3   6  90  12
4   7  78  34

In [19]: np.where(df.c == 90, 88, df.b)                                                                       
Out[19]: array([10,  6, 88, 90, 78])

In [20]: df.b = np.where(df.c == 90, 88, df.b)                                                                

In [21]: df                                                                                                   
Out[21]: 
    a   b   c
0  10  10  55
1   4   6  55
2   5  88  90
3   6  90  12
4   7  78  34

In [22]: np.where(df.b == 88, 67, df.c)                                                                       
Out[22]: array([55, 55, 67, 12, 34])

In [23]: df                                                                                                   
Out[23]: 
    a   b   c
0  10  10  55
1   4   6  55
2   5  88  90
3   6  90  12
4   7  78  34

In [24]: df.c = np.where(df.b == 88, 67, df.c)                                                                

In [25]: df                                                                                                   
Out[25]: 
    a   b   c
0  10  10  55
1   4   6  55
2   5  88  67
3   6  90  12
4   7  78  34
```

```python
In [26]: df2                                                                                                  
Out[26]: 
   a   b   c
0  1  45  45
1  4   6  68
2  5  78  90
3  6  90  12
4  7  78  34

In [27]:    
```