###**Formated strings usage with :.xf, :xd, :x**

##I knew this before but I decided to remind myself about these features, so:

#**:.xf**  where x is any number

Allows you to pad float object with x digits after decimal number
```python
p = 3.14159265
print(f"{p:2f}") # will output 3.14
```
#**:xd** where x is any character

Allows you to pad an integer with a chosen character until its length reaches x
```python
p = 3
print(f"{p:02d}") # will output 003
```

#**:xy** where y is any num, x is any character

Works like :xd but :xy pad object after it
