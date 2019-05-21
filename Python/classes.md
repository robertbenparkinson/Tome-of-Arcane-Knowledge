# Python Classes

## Class Example

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def myfunc(self):
        print("Hello my name is " + self.name)

p1 = Person('Code Monkey', 42)
print(p1.name)
print(p1.age)
p1.myfunc()

> "Code Monkey"
> 42
> "Hello my name is Code Monkey"

```