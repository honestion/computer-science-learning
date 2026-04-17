###**Constants' and variables' scope**
#Constants should be initialized outside of main fuction but main's local variables should be intialized inside of main function
```python
LST = [1, 2, 3] #const is out of main
def main():
  cond = True # local variable is inside of main
  if   LST[2] > 3:
    cond = False #There it will be true
