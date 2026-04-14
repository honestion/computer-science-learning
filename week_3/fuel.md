###**return = break**

#return keyword breaks the loop in function
```python
def get_int():
  while True:
    try:
      x = int(input())
      return x # return will break the while loop
      # so break is not necessary
    except ValueError:
      pass
