## TypeError: 'numpy.ndarray' object is not callable


df.values() -> df.values itself is of type **numpy.ndarray**.


## Examples

```python
In [5]: pd.__dict__.get('Panel')                                                                                       
Out[5]: pandas.Panel

In [6]: pd.__dict__.get('Panel').__dict__                                                                              
Out[6]: 
mappingproxy({'__module__': 'pandas',
              '__dict__': <attribute '__dict__' of 'Panel' objects>,
              '__weakref__': <attribute '__weakref__' of 'Panel' objects>,
              '__doc__': None})

In [7]: pd.__version__                                                                                                 
Out[7]: '0.25.0'

In [8]: df = pd.DataFrame([{'a': 12, 'b': 34, 'c': 56}, {'a': 45, 'b': 54, 'c': 23, 'e': 67}])                         

In [9]: df                                                                                                             
Out[9]: 
    a   b   c     e
0  12  34  56   NaN
1  45  54  23  67.0

In [10]: df.fillna(0, inplace=True)                                                                                    

In [11]: df                                                                                                            
Out[11]: 
    a   b   c     e
0  12  34  56   0.0
1  45  54  23  67.0

In [12]: df.T                                                                                                          
Out[12]: 
      0     1
a  12.0  45.0
b  34.0  54.0
c  56.0  23.0
e   0.0  67.0

In [13]: df.T.to_dict()                                                                                                
Out[13]: 
{0: {'a': 12.0, 'b': 34.0, 'c': 56.0, 'e': 0.0},
 1: {'a': 45.0, 'b': 54.0, 'c': 23.0, 'e': 67.0}}

In [14]: df.T                                                                                                          
Out[14]: 
      0     1
a  12.0  45.0
b  34.0  54.0
c  56.0  23.0
e   0.0  67.0
```

```python
In [15]: df.values()                                                                                                   
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-15-57e850d2cc5f> in <module>
----> 1 df.values()

TypeError: 'numpy.ndarray' object is not callable

In [16]: df.T.to_dict().values()                                                                                       
Out[16]: dict_values([{'a': 12.0, 'b': 34.0, 'c': 56.0, 'e': 0.0}, {'a': 45.0, 'b': 54.0, 'c': 23.0, 'e': 67.0}])

In [17]: l = df.T.to_dict().values()                                                                                   

In [18]: l = list(df.T.to_dict().values())                                                                             

In [19]: l                                                                                                             
Out[19]: 
[{'a': 12.0, 'b': 34.0, 'c': 56.0, 'e': 0.0},
 {'a': 45.0, 'b': 54.0, 'c': 23.0, 'e': 67.0}]

In [20]: l.pop(0)                                                                                                      
Out[20]: {'a': 12.0, 'b': 34.0, 'c': 56.0, 'e': 0.0}

In [21]: l                                                                                                             
Out[21]: [{'a': 45.0, 'b': 54.0, 'c': 23.0, 'e': 67.0}]

In [22]: l.pop(-1)                                                                                                     
Out[22]: {'a': 45.0, 'b': 54.0, 'c': 23.0, 'e': 67.0}

In [23]: l                                                                                                             
Out[23]: []

In [24]: l.pop(-1)                                                                                                     
---------------------------------------------------------------------------
IndexError                                Traceback (most recent call last)
<ipython-input-24-971cd78094bc> in <module>
----> 1 l.pop(-1)

IndexError: pop from empty list

In [25]: type(df.T)                                                                                                    
Out[25]: pandas.core.frame.DataFrame

In [26]: type(df)                                                                                                      
Out[26]: pandas.core.frame.DataFrame

In [27]: type(pd.Series())                                                                                             
Out[27]: pandas.core.series.Series

In [28]: df.to_dict()                                                                                                  
Out[28]: 
{'a': {0: 12, 1: 45},
 'b': {0: 34, 1: 54},
 'c': {0: 56, 1: 23},
 'e': {0: 0.0, 1: 67.0}}

In [29]: df.values                                                                                                     
Out[29]: 
array([[12., 34., 56.,  0.],
       [45., 54., 23., 67.]])

In [30]: df                                                                                                            
Out[30]: 
    a   b   c     e
0  12  34  56   0.0
1  45  54  23  67.0

In [32]: df.loc[df['c'] == 56, 'b'] = 10                                                                               

In [33]: df                                                                                                            
Out[33]: 
    a   b   c     e
0  12  10  56   0.0
1  45  54  23  67.0

In [34]: df.loc[df.c == 23, 'b'] = 10                                                                                  

In [35]: df                                                                                                            
Out[35]: 
    a   b   c     e
0  12  10  56   0.0
1  45  10  23  67.0

In [36]:                    

```