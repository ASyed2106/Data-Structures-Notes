# Tuples
  What is it even???
    - Strings and Lists are basic iterable data types that are very similar with key differences:
    - Strings only allow alphanumeric characters and special symbols to represent text
    - Lists allow all data types as its items/members 
    - Strings are immutable whereas Lists are mutable
    - These significant differences cause a headache when you require the following data structure:
            It must be immutable
            It must allow different datatypes as items
            It must be iterable
            It must be nestable (much like a list within a list)
            ***All of these are solved with a data structure called: Tuple***

How to use??
   - Tuples are declared with parenthesis ( round brackets)
         () is an empty tuple
   - (50,) is a singleton tuple; the comma is required
   - ***Tuples are sliceable; therefore, indexable using square brackets***
   - A singleton is an iterable data structure with only single item.

### Example
```python
tup = ('C', ' Java', 'Python')
empty_tup = ()
single_tup = ('Park',)

print(tup)
print(empty_tup)
print(single_tup)
```
outputs:
('C', ' Java', 'Python')
()
('Park',)

## Tuple operators
```python
# Concatenation: Joining two tuples
a = (1,2,3)
b = (4,5,6)
concat_result = a + b
print('a+b:', concat_result)


# Repetition: Repeating a list multiple times
c = ('Hi!',)
repet_result = c * 3
print('c*3', repet_result)

# Membership: Check if a value exists in a tuple
d = a + b + c
print('d:', d)
print('\'Hi!\' in d:', 'Hi!' in d)
print('7 in d:', 7 in d)
```
outputs:
a+b: (1, 2, 3, 4, 5, 6)
c*3 ('Hi!', 'Hi!', 'Hi!')
d: (1, 2, 3, 4, 5, 6, 'Hi!')
'Hi!' in d: True
7 in d: False
