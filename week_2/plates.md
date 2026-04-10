##**# Break is very important, because without it cycle goes next element, consequently the only last element has checked**
```python
numbers = [1,2,5,13]
condition = True # flag-variables need to be initialized at the beginning of cycle
for number in numbers:
  if str(number) not in "0123456789":
    condition = False
    break # without break -> a = True
    
