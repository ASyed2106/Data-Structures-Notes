## Map Function

- The idea of a map function is to apply a function to an iterable data.
    Formatting:
        map(function_name, sequence)
        function_name: any function (built-in or selfmade) that returns a desired value of choice
         sequence: any iterable data type
         
``` python

def square(num):
    ''' squares the given num argument '''
    return num ** 2
# end of square

array = list(range(1,11))
square_array = list(map(square, array))

print('Original Array:', array)
print('Array Squared:', square_array)
```
Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Array Squared: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

 ***Map function is that it doesn’t return a specific data type, but rather, an python iterable data.
 Therefore, after we apply the map function, we just execute a list function on it.***

### Example
 ```python
 
 
def upper(x):
    ''' upper() turns string x into its uppercased counter part '''
    return x.upper()

word = 'hello world!'
upper_word = ''.join(list(map(upper, word)))

print(word)
print(upper_word)

# simpler way:
print(word.upper())
```
^^^ Is example of how you shouldn’t use map() for every little changes you want to a string.
    This also applies to all data structure that has methods. 
    You don’t want to use methods with map, since there is a high probablity that there is already method for what you might want to do.

## Filter function
- filter out items from a data set that meets a certain condition.
    Formatting:
        filter(bool_returning_function, sequence)
        function: The function name we provide for filter() must be return a boolean value 
                  should also be able handle the items inside the sequence as its arguments
        sequence: any iterable data type
### Example
```python

def isOdd(x):
    ''' isOdd() returns True if x is odd.'''
    return x % 2 != 0

array = list(range(1,101))
odds = list(filter(isOdd, array))

print('Odd Numbers from 1 to 100:', odds)
```
### Another example

``` python
# Palindromic Numbers from 1 to 10000

def isPalindrome(x):
    ''' isPalindrome returns True if string X is a palindrome.'''
    return x == x[::-1]

array = list(range(1,10000))

palindromic_numbers = list(map(int, filter(isPalindrome, map(str, array))))
print('Palindromic Numbers from 1 to 10,000', palindromicNumbers)
```
### What is going on???

-  string version of the array --> map(str, array)
-  filter out the palindrome --> filter(isPalindrome, string version of the array)
-  remap all values back to integers --> map(int, palindromes)
-  turn the mapped integers iterable back inside a list --> list(palindromicIterables)

How it would looked with multiple defined variables:

array = list(range(1,10000))
str_array = map(str, array)
palindromes = filter(isPalindrome, str_array)
palindromics = map(int, palindromes)

palindromic_numbers = list(palindromes)

##Composition of Functions
- idea of using functions within a function call or apply one function to the result of another function.
