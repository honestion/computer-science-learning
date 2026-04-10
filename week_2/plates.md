##**# Break is very important, because without it cycle goes next element, consequently the only last element has checked**
```python
numbers = [1,2,5,13]
condition = True # flag-variables need to be initialized at the beginning of cycle(called "Default to True")
for number in numbers:
  if str(number) not in "0123456789":
    condition = False
    break # without break -> a = True
```
    
##**#Slices**

#Slices allow you to get elements of the list fast. To use slices you need to use ":" inside square brackets. Slices work like "list[start:stop:step];

```python
numbers = [1, 2, 5, 13]
def get_even_indexes(items): #not recommended to use def func(list) - because list it's datatype
  return items[::2] # return elements with index 0, 2, 4, 6, etc.
get_even_indexes(numbers) # 1, 5(even indexes in programming not in real life)

numbers[::-1] # whole list in reverse order

```
##**#if I want to describe, what function do, I need to use triple '(''' description ''')**

##**#.append() returns None like .remove()(Mutating methods) and .sort(), .extend(), .clear()** 
#So if want:
```python
for char in number:
  if char in "0123456789":
    inter_list = inter_list.append(char) #  is not correct
    '''I should just write inter_list.append()'''
