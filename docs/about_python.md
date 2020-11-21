what is my python version:
```python
import sys
sys.version
```

float info, largest and smallest numbers available by float:
```python
 sys.float_info
 ```
## Strings:
strings are **immutable** so you can not change the value of the string, but you can create new string:
```python
name = [Micheal jackson]
name[0] = 'j'                   # it is incorrect
name  = name + 'is the best'    # correct
```
string | result
------ |-------
\n    |  new line
\t    | tab
\\  | print a backslash

```
# using r :
# r will tell python that string will be display as raw string

print(r"this will print a backslash \ in the output")
```
stride, Use a stride value of 2 to print out every second character of the string `name`:
```
mame = "012345678"
name[::2] # is equal to '02468'
# or
name[0:9:2]
```

![aliasing](images/aliasing.png)

## in dictionaries
Keys can also be any immutable object such as a tuple

Keys can only be strings, numbers, or tuples, but values can be any data type.

## [Mutable vs Immutable Objects in python](https://medium.com/@meghamohan/mutable-and-immutable-side-of-python-c2145cf72747#:~:text=Everything%20in%20Python%20is%20an%20object.&text=Simple%20put%2C%20a%20mutable%20object,set%2C%20dict\)%20are%20mutable.)

## [Aliasing in python](https://v4.software-carpentry.org/python/alias.html#:~:text=In%20Python%2C%20aliasing%20happens%20whenever,that%20store%20references%20to%20values.)
because variables are just names that store references to values.
