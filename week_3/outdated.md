# You need to to do lst[obj]
I made a wierd mistake when initialized value into whole list:
```python
lst = ['q', 'qe', 'egfd']
lst[1] = lst[1].strip('e') # the 2nd element will be 'q'
#so
lst = lst[1].strip(',') # is a mistake because the whole list will be this value
```
