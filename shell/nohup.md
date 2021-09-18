
````bash

In [1]: '&'.join(f'nohup sh {i}.sh ' for i in range(1, 7))                                                                        
Out[1]: 'nohup sh 1.sh &nohup sh 2.sh &nohup sh 3.sh &nohup sh 4.sh &nohup sh 5.sh &nohup sh 6.sh '

In [2]: '&'.join(f'nohup sh {i}.sh ' for i in range(1, 7)).strip()                                                                
Out[2]: 'nohup sh 1.sh &nohup sh 2.sh &nohup sh 3.sh &nohup sh 4.sh &nohup sh 5.sh &nohup sh 6.sh'
```
