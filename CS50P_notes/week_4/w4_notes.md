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
## **What is "raise_for_error" function**
If you call, for example, **requests.get()** server will asnwer with exit code like 2.. , 4.., or 5.. but codes
started with 4 and 5 mean *errors*. It's important because even if there are 4 or 5 exit code of request.get()
will be executed anyway so at the end you will get wrong output. But if you use **raise_for_error()** there will
be **HTTPError** from **requests.RequestException** and programm will, for instance, exit. So **raise_for_error()**
allows you to not work with "garbage" but throw it out:
```python
import requests

try:
  url = ...

  response = requests.get(url)
        
  response.raise_for_status()
  # if there is exit code 5..(server error) or 4..(client error) func will return error

  # if we are there means that there are no errors
  data = response.json()
  
except requests.RequestsException:
  print(...) # some explanation
  sys.exit(1)
```