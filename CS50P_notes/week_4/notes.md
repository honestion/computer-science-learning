## **Function can return 2 values per time**
Function can return 2 values per time so
```python
def main():
  first_num, second_num = get_ints() # first_num = x, second_num = y

def get_ints():
while True:
  try:
    x = int(input()) 
    y = int(input())
    return x, y
  except ValueError:
    continue

if __name__ == "__main__":
  main()
```
## **Instead of using many checks type of "a == 1 or a == 2 ..." better use "in" keyword**
Immideately to example:
```python
try:
  a = int(input())
except ValueError:
  print("Not int")

# Instead of
if a == 1 or a == 2 or a == 3:
 print("+")
else:
 print("-")
# better use
if a in [1, 2, 3]: # but not str because if you use |str(a) in "123" | there are 12 and 23
  print("+")       # in this string so if a == 12 or a == 23 output will be + not -
else:
  print("-")
```
