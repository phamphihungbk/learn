# Python: OOP

- [`self vs cls`](#self-vs-cls)
- [`__call__`](#__call__)

[↑ top](#python-oop)
<br><br><br><br><hr>

### `self vs cls`

<br>

- cls belongs to the class (static method)
- self refer to `instance of class`

[↑ top](#python-oop)
<br><br><br><br><hr>

### `__call__`

<br>

> this method enables to write classes where the instances behave like functions
> and can be called like a function

```python
class Example:
    def __init__(self):
        print("Instance Created")

    # Defining __call__ method
    def __call__(self):
        print("Instance is called via special method")

# Instance created
e = Example()

# __call__ method will be called
e()

# Instance Created
# Instance is called via special method
```

[↑ top](#python-oop)
<br><br><br><br><hr>
