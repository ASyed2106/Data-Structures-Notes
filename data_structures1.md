## Matrices and List Comprehension

- Matrices are representations of numbers, symbols, or expressions in a 2-Dimensional Array.
- In com sci, ewe can start to create a data structure that has values in rows and columns, much like a table, by utilizing a list within a list. 
- This is crucial for fields in Calculus, Vectors, and Linear Algebra.

### Example of matrix in python
``` python
matrix_A = [
    [1, 2, 3, 4],
    [5, 6, 7, 8]
]

# Accessing Matrix A
print('Row 1: %s' % matrix_A[0]) # Recall: Indexing starts at zero in Python
print('Value at Row 2 Column 2: %s' % matrix_A[1][1])
```

###In Python 3, there is no data structure called a "Matrix".

Therefore, we are programming a list within a list and following the rules of a regular matrix:
- All rows must have the same number of values
- All columns must have the same number of values
- All items in the 2D List must have the same data types
- Since indexing always starts at 0 ... row 1 is technically located at matrix_A[0]

List comprehension

```python
# Old Method
squares = []
for i in range(10):
    squares.append(i ** 2)

print('Our result: %s' % squares)```

Our result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

```python

# List Comprehension

squares = [i**2 for i in range(10)]

print('Our new result: %s' % squares)
```
Our new result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

### Whats happening exactly? 
- A Square Bracket containing an expression that describes the list 
- One or more For clause to explain its members
-Then a zero or more if clauses depending on the complexity of the list
  Examine: [i**2 for i in range(10)]
      i**2 for i in range(10) --> is the expression that describe the list
      i**2 describes each item in the list
      i is taken from the for clause
      for i in range(10) describes where i comes from
