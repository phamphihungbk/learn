# Python: Data Types

- [`set`](#set)
- [`sequence`](#sequence)
- [`mapping`](#mapping)

[↑ top](#python-data-types)
<br><br><br><br><hr>

### `set`

<br>

**frozenset**

```python
fruits = {"Apple", "Banana", "Cherry", "Apple", "Kiwi"}
basket = frozenset(fruits)

print('Unique elements:', basket)

# Add new fruit throws an error!
basket.add("Orange")
print('After adding new element:', basket)

# AttributeError: 'frozenset' object has no attribute 'add'

```

frozenset is immutable data type and can't add new element

<br>

**set**

```python
fruits = {"Apple", "Banana", "Cherry", "Apple", "Kiwi"}

print('Unique elements:', fruits)

# Add new fruit
fruits.add("Orange")
print('After adding new element:', fruits)

# Size of the set
print('Size of the set:', len(fruits))

>> size
7

```

[↑ top](#python-data-types)
<br><br><br><br><hr>

### `sequence`

> - tuple is immutable, list is mutable
> - tuple is faster and consume less memory than list
> - should not define a list in tuple

<br>

**tuple**

```python
# code to test that tuples are immutable

tuple = (0, 1, 2, 3)
tuple[0] = 4
print(tuple)

# TypeError: 'tuple' object does not support item assignment

```

tuple is immutable data type and can't add new element

<br>

**list**

```python
# Creating a List with
# the use of Numbers
# code to test that tuples are mutable
List = [1, 2, 4, 4, 3, 3, 3, 6, 5]
print("Original list ", List)

List[3] = 77
print("Example to show mutablity ", List)

# Original list  [1, 2, 4, 4, 3, 3, 3, 6, 5]
# Example to show mutablity  [1, 2, 4, 77, 3, 3, 3, 6, 5]

```

[↑ top](#python-data-types)
<br><br><br><br><hr>

### `mapping`
> - OrderedDict is a subclass of dict object
> - it maintains the orders of keys as inserted

<br>

**dict**

```python
#Create normal dict
my_dict = {}
my_dict['AA'] = 11
my_dict['BB'] = 22
my_dict['CC'] = 33
my_dict['DD'] = 44

for item in my_dict.items():
   print(item)

# ('AA', 11)
# ('CC', 33)
# ('BB', 22)
# ('DD', 44)

```

<br>

**OrderedDict**

```python
import collections

#Create ordered dict
my_ord_dict = collections.OrderedDict()
my_ord_dict['AA'] = 11
my_ord_dict['BB'] = 22
my_ord_dict['CC'] = 33
my_ord_dict['DD'] = 44

for item in my_ord_dict.items():
   print(item)

# ('AA', 11)
# ('BB', 22)
# ('CC', 33)
# ('DD', 44)

```

<br>

[↑ top](#python-data-types)
<br><br><br><br><hr>
