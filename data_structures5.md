# Dictionary 
  - Dictionary (Associative Array, map, symbol table) is a data type that stores a collection of (key, value) pairs, such that each possible key appears at most once in the collection.

## Common Operations:
  - Adding a pair
  - Removing a pair
  - Modify an existing pair
  - Lookup of a value associated with a particular key
  - Aside: This concept is an introduction to concepts similar to: hash table and search trees

Defining a Dictionary 
  - Dictionaries also use {} like sets; however, their individual item format is very different.
  - Each item in a dictionary be a pair of key: value.

``` python 
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

# There are 3 items: each with their unique addresses and value
# Accessing
print('Sammy dict:', sammy)
print('Username:', sammy['username'])
print('Online Status:', sammy['online'])
print('Follower Count:', sammy['followers'])
```
### outputs:
Sammy dict: {'username': 'sammy', 'online': True, 'followers': 42}
Username: sammy
Online Status: True
Follower Count: 42
Dictionary Properties
Each item in a dictionary is a key, value pair.

## Keys
  - Keys are unique address for a dictionary value’s location

### Key Properties:
  - Must be immutable (strings, numbers, tuples, frozenset)
  - Unique; therefore, two same key values cannot exist in a single dictionary
  - NEWEST CREATED ITEM with a duplicate KEY superceeds the previous declaration

### Values
  - Values of a dictionary within a key can be any data type.

## Updating a Dictionary
  - We can modify existing values by referencing the key
  - We can add new values to a dictionary by creating a new key
  - We can overwrite a value at an existing key by referencing and recreating the value for it

### Update Example

``` python
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

sammy['followers'] += 10 # We are adding 10 to the value located at key: 'followers'
sammy['verified'] = True # We added a new value at a new key: 'verified'
sammy['username'] = 'SammySammy'
print('Sammy Dict:', sammy)
```
### outputs: 
Sammy Dict: {'username': 'SammySammy', 'online': True, 'followers': 52, 'verified': True}

## Deletion with Dictionary
  - We can delete a key hence deleting the value connected to the key
  - We can empty out the entire dictionary
  - We can delete the dictionary (uncommonly used)
``` python
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

del sammy['followers'] # del is a keyword used to help us to execute a removal
print('followers key deleted:', sammy)

sammy.clear() # {} is considered an empty dict
print('emptying out a dictionary', sammy)
print('--\n\n')

del sammy
print('Deleting sammy, should create an error when referenced again', sammy)
```

## Dictionary Methods
  - To help power this awesome data structure, it has good set of methods for us to use.
  - Let A and B be a dictionary
      A.keys() –> Returns a sequence of keys/addresses in A
      A.values() –> Returns a sequence of item values in A
      A.items() –> Returns a sequence of key,item pairs in A
      A.get(address) –> Returns the item value at address
      A.update(B) –> Extends A with the dictionary of key,value pairs of B
