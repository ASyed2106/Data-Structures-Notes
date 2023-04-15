# Sets
  - A set is an unordered collection with no duplicate elements in Python 3.
  - Set is a mathematical way to describe collection of different unique objects.
  - By following the operations and characteristics of the mathematical set, we can utilizie such data structure in our Python code.

Defining sets
```python
example_set1 = {1, 2, 3}
example_set2 = {'h','e','l','l','o'}

print('example_set1:', example_set1)
print('example_set2:', example_set2) # Notice there is only 1 'l'; Also notice the order of the values outputted
print('--')

singleton_set = {7}
empty_set = set() # this is because {} is reversed for a different feature in python 3.

print('Singleton:', singleton_set)
print('Empty Set:', empty_set)
```
ouputs:
example_set1: {1, 2, 3}
example_set2: {'o', 'e', 'h', 'l'}
--
Singleton: {7}
Empty Set: set()
Basic Built-in Functions w/ Sets

## Basic Built-in Functions w/ Sets
``` python
example_set = set('hello') # set() turns an iterable into a set
print('example_set:', example_set)
print('--')

print('Number of Values:', len(example_set)) # length function
print('Minimum Value:', min(example_set)) # min function
print('Maximum Value:', max(example_set)) # max function
print('--')

# tuple to set
tup = (2,3,5,7)
print('tup to set:', set(tup))

# list to set
array = ['orange']*2 +  ['watermelon', 'apple'] + ['kiwi'] * 10
print('Original Array:', array)
print('list to set:', set(array))
```
outputs:
example_set: {'o', 'e', 'h', 'l'}
Number of Values: 4
Minimum Value: e
Maximum Value: o
tup to set: {2, 3, 5, 7}
Original Array: ['orange', 'orange', 'watermelon', 'apple', 'kiwi', 'kiwi', 'kiwi', 'kiwi', 'kiwi', 'kiwi', 'kiwi', 'kiwi', 'kiwi', 'kiwi']
list to set: {'watermelon', 'orange', 'apple', 'kiwi'}

## Basic Membership Operators
  - Membership is one of the key operations with set because:
      A set has no duplicates
      A set’s membership operation is one of the fastest operations compared to strings, lists, or tuples this will be covered more when we look at the concept of: complexity
      By using membership operator, we can be certain a target exists or does not exist in our data

### Membership Example
``` python
example_set = set('hello')
print("Membership of: \'h\'", 'h' in example_set)
print("Non-Membership of: \'z\'", 'z' not in example_set)
``` 
Membership of: 'h' True
Non-Membership of: 'z' True

## Accessing Values in a Set
  - Due to its unordered nature of a set, there is no concept of indexing or slicing with a set.
  - Set is however iterable.
 ``` python
# Iteration of a Set
example_set = {2,3,5,7,11,13}

for v in example_set:
    print('Values of example_set:', v)
 ```
 
 ouputs: 
Values of example_set: 2
Values of example_set: 3
Values of example_set: 5
Values of example_set: 7
Values of example_set: 11
Values of example_set: 13

##Python 3 Sets are mutable: Adding and Removing Values
   - Sets are mutable; therefore, we can add and remove values
   - There are also methods much lists that can affect the original sets as well

### Examples
``` python
# Adding and Removing Values
languages = set() # empty set initialization

programming_languages = ['C', 'C#', 'Java', 'Python', 'HTML', 'CSS', 'JavaScript', 'Haskell']

for item in programming_languages:
    languages.add(item) # .add() method adds an item to a set

print('Languages set:', languages)
print('--')

languages.discard('HTML') # looks for the target value, if found, it will remove from the set
print('HTML deleted:', languages)

languages.remove('CSS') # remove can be used to delete a value;
# only difference is it will raise an error if the target is not found
print('CSS deleted:', languages)

random_remove = languages.pop() # .pop() method deletes a random value and return the value ... not recommended
print('Randomly Removed value:', random_remove)

languages.clear() # .clear() will empty out a set : output is set()
print('Empty languages:', languages)
```
## Powering Up Sets: Set Operators
  - Much like its mathematical counterpart, sets in Python 3 can utilize its vast operators to help us do complex calculations.
  - Most of these operators will have a method counterpart because sets are mutable.

Our Operators
    - Union
          The joining/combining of two sets.
    - Intersection
          Members/Items that only exists in both sets.
    - Difference
          Members/items that only exists in the first set and not the second set.
    - Symmetric Difference
          Members/items that exists one or the other set, but not both sets
    - Proper Subset
          This is a boolean operator.
    - Subset
          This is a boolean operator
    - Proper Superset
          This is a boolean operator
    - Superset
          This is a boolean operator
