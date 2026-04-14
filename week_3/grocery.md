### **.get() method and it's usage**
## .get() 
.get() method allows you to get dictionary value by it's key. But huge .get() advantage is that there 
would be no KeyError if key is not in dictionary
```python
lst = {"zero": 0, "one": 1, "two": 2}
a = lst.get("four") # There will returns None becuse its default value of .get()
b = lst.get("eight", "No such index") # And there will returns "No such index"
``` 
so I can use .get() to count elements is a list
```python

 