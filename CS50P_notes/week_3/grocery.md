## **.get() method and it's usage**

.get() method allows you to get dictionary value by it's key. But huge .get() advantage is that there 
would be no KeyError if key is not in dictionary
```python
lst = {"zero": 0, "one": 1, "two": 2}
a = lst.get("four") # There will returns None becuse its default value of .get()
b = lst.get("eight", "No such index") # And there will returns "No such index"
``` 
so I can use .get() to count elements in a list with dublicated elemets
```python
lst = [0, 1, .1, 2]
counts = {}
for elem in lst:
    counts[elem] = lst.get(elem, 0) + 1 # .get() takes index from lst(start from zero) -> the 1 element was 1 time
```
## 'for' loop can be forcibly started with 'or [None]'

you can start 'for' loop forcibly if list, where 'for' iterates, is empty, so
```python
lst = []
for i in lst: # This loop will not iterate because the list is empty
    pass
```
but
```python
lst = []
for i in lst or [None]: # This loop will iterate at least 1 time
    pass