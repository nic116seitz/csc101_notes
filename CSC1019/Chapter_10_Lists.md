## Basics
- lists are one of the most important and often-used types in python
- 2 terms used to define lists
- #container : is an object that groups related objects together
- #mutable : the size of the list can grow or shrink and the elements within the list can change
- list is a sequence, thus there is a left to right positional order
- each element in a list can be a different object type such as str, int, float or even other lists
- you can create a list using the builtin list()
- this function accepts a single iterable object argument such as a string list or tuple and returns new obj
## Common list operations and in-place list modification
- Unlike the str sequence type a list is mutable meaning a list can grow and shrink without replacing the entire list with an updated copy
- Such growing and shrinking capability is called #in-place-modification 

Table 10.1.1: Some common list operations.

| Operation           | Description                                                           | Example code                                             | Example output  |
| ------------------- | --------------------------------------------------------------------- | -------------------------------------------------------- | --------------- |
| my_list = [1, 2, 3] | Creates a list.                                                       | my_list = [1, 2, 3]<br>print(my_list)                    | [1, 2, 3]       |
| list(iter)          | Creates a list.                                                       | my_list = list("123")<br>print(my_list)                  | ['1', '2', '3'] |
| my_list[index]      | Gets an element from a list.                                          | my_list = [1, 2, 3]<br>print(my_list[1])                 | 2               |
| my_list[start:end]  | Gets a _new_ list containing some of another list's elements.         | my_list = [1, 2, 3]<br>print(my_list[1:3])               | [2, 3]          |
| my_list1 + my_list2 | Gets a _new_ list with elements of my_list2 added to end of my_list1. | my_list = [1, 2] + [3] <br>print(my_list)                | [1, 2, 3]       |
| my_list[i] = x      | Changes the value of the element at index i in-place.                 | my_list = [1, 2, 3]<br>my_list[2] = 9 <br>print(my_list) | [1, 2, 9]       |
| del my_list[i]      | Deletes the element from index i from a list.                         | my_list = [1, 2, 3]<br>del my_list[1]<br>print(my_list)  | [1, 3]          |

- The difference between in-place modification of a list is important. In-place modification affects any variable that references the list and can have unintended side effects
- It is important to note that when you have two objects referencing the same list if that list is changed by one object it changes for both
- In the case that you want to have a copy of one list that changes from the original list would be to create a copy using the slice notation without any indices
- `list_copy = list_original[:]` This  is the way that you would do said copy
# **List Methods**
## Common list methods
- a #list_method can perform useful operations on a list


able 10.2.1: Available list methods.

**Adding elements**

| List method       | Description                             | Code example                                 | >Final my_list value |
| ----------------- | --------------------------------------- | -------------------------------------------- | -------------------- |
| list.append(x)    | Add an item to the end of list.         | `my_list = [5, 8]   my_list.append(16)`      | [5, 8, 16]           |
| list.extend([x])  | Add all items in [x] to list.           | `my_list = [5, 8]   my_list.extend([4, 12])` | [5, 8, 4, 12]        |
| list.insert(i, x) | Insert x into list _before_ position i. | `my_list = [5, 8]   my_list.insert(1, 1.7)`  | [5, 1.7, 8]          |
  
**Removing elements**

| List method    | Description                                   | Code example                                  | Final my_list value           |
| -------------- | --------------------------------------------- | --------------------------------------------- | ----------------------------- |
| list.remove(x) | Remove first item from list with value x.     | `my_list = [5, 8, 14]   my_list.remove(8)`    | [5, 14]                       |
| list.pop()     | Remove and return last item in list.          | `my_list = [5, 8, 14]   val = my_list.pop()`  | [5, 8]<br><br>  <br>val is 14 |
| list.pop(i)    | Remove and return item at position i in list. | `my_list = [5, 8, 14]   val = my_list.pop(0)` | [8, 14]<br><br>  <br>val is 5 |

  
**Modifying elements**

| List method    | Description                            | Code example                               | Final my_list value |
| -------------- | -------------------------------------- | ------------------------------------------ | ------------------- |
| list.sort()    | Sort the items of list in-place.       | `my_list = [14, 5, 8]   my_list.sort()`    | [5, 8, 14]          |
| list.reverse() | Reverse the elements of list in-place. | `my_list = [14, 5, 8]   my_list.reverse()` | [8, 5, 14]          |

**Miscellaneous**

| List method    | Description                            | Code example                               | Final my_list value |
| -------------- | -------------------------------------- | ------------------------------------------ | ------------------- |
| list.sort()    | Sort the items of list in-place.       | `my_list = [14, 5, 8]   my_list.sort()`    | [5, 8, 14]          |
| list.reverse() | Reverse the elements of list in-place. | `my_list = [14, 5, 8]   my_list.reverse()` | [8, 5, 14]          |
# Iterating over a list
## List iteration
- For loop is designed for this
- Consider `for my_var in my_list:` 
	- Each iteration for the loop creates a new variable by binding the next element for the list to the name my_var
## IndexError and enumerate()
- Common error is to try to access a list with an index that is out of the lit's index range
- This will trigger an #IndexError
- #enumerate function iterates over a list and provides an iteration counter.
- enumerate syntax:
	- `for x in enumerate(iterable, start=start_num):`
	- In the above syntax example x represents each item you are iterating over
	- iterable represents the collection of iterables being iterated on 
	- start represents the count you want your enumeration to start with (by default it starts at 0) 

## Built-in functions that iterate over lists
- iterating though a list to find or calculate certain values like the min/max or sum is so common that python provides builtin functions as shortcuts
- Instead for writing a for loop and tracking a max for example or adding a sum a programmer can use a statement such as `max(my_list)`


Table 10.3.1: Built-in functions supporting list objects.

| Function  | Description                                                            | Example code                                    | Example output |
| --------- | ---------------------------------------------------------------------- | ----------------------------------------------- | -------------- |
| all(list) | True if every element in list is True (!= 0), or if the list is empty. | `print(all([1, 2, 3]))   print(all([0, 1, 2]))` | True<br>False  |
| any(list) | True if any element in the list is True.                               | `print(any([0, 2]))   print(any([0, 0]))`       | True<br>False  |
| max(list) | Get the maximum element in the list.                                   | `print(max([-3, 5, 25]))`                       | 25             |
| min(list) | Get the minimum element in the list.                                   | `print(min([-3, 5, 25]))`                       | -3             |
| sum(list) | Get the sum of all elements in the list.                               | `print(sum([-3, 5, 25]))`                       | 27             |
# List nesting
- Since a list can contain any type of obj as an element, and a list is itself an obj, a list can contain another list as an element
- Such embedding is known as #list_nesting
- To access indexes of a list within a list you would add a second value to the indexing
- EX:
- `my_list[nested_list_pos][pos_within_nested_list]`
- List is a single-dimensional sequence of items, like a series of times, data samples etc
- List nesting allows for a programmer to also create a #multi-dimesional_data_structure 
	- The simplest of these would be a two-dimensional table, like a spreadsheet or tic-tac-toe
- A programmer can access all of the elements of nested lists by using #nested_for_loops The first loop iterates through the elements of the outer list, while the nested loop iterates through the inner list elements
- Outer loop assigns the variable row with one of the list elements
- Inner loop iterates over the elements of that list
- *To learn this consider playing with nested loops and multi dimensional lists*
# List slicing
- A programmer can use #slice_notation to read multiple elements form a list, creating a new list that contains only the desired elements
- anything before `:` indicates the first element to read
- anything after indicates the last element to read
- end position is not included in the produced list
- you can also use negative indices to specify the end of the range to be sliced  
- If you specify any number longer than the length of the list the slice will include up to the last number in the list
- #stride allows you to decide by what number the slice is counting by this is specified by the third number in the slice notation
- EX:
- `[starting_num:end_num:stride`


## **Common list slicing operations**


| Operation                 | Description                                                     | Example code                                            | Example output      |
| ------------------------- | --------------------------------------------------------------- | ------------------------------------------------------- | ------------------- |
| my_list[start:end]        | Get a list from start to end (minus 1).                         | `my_list = [5, 10, 20]   print(my_list[0:2])`           | [5, 10]             |
| my_list[start:end:stride] | Get a list of every stride element from start to end (minus 1). | `my_list = [5, 10, 20, 40, 80]   print(my_list[0:5:3])` | [5, 40]             |
| my_list[start:]           | Get a list from start to end of the list.                       | `my_list = [5, 10, 20, 40, 80]   print(my_list[2:])`    | [20, 40, 80]        |
| my_list[:end]             | Get a list from beginning of the list to the end (minus 1).     | `my_list = [5, 10, 20, 40, 80]   print(my_list[:4])`    | [5, 10, 20, 40]     |
| my_list[:]                | Get a copy of the list.                                         | `my_list = [5, 10, 20, 40, 80]   print(my_list[:])`     | [5, 10, 20, 40, 80] |


# Tuple basics
## Tuples
- #tuple stores a collection of data like a list but is immutable
- once created element's cannot be changed
- is a sequence type
- A new tuple is generated by creating a list of comma separated values such as 5, 15, 20
- Typically tuples are surrounded with parentheses 
- Good for use cases where you want to make sure that values don't change
- Typically used when element position is important
## Named tuples
- #named_tuple allows programmer to define a new simple data type that consists of named attributes
Below is the syntax for creating a named tuple:




|                                                                                                                                                                                                                                                                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| from collections import namedtuple<br><br>Car = namedtuple("Car", ["make","model","price","horsepower","seats"])  # Create the named tuple<br><br>chevy_blazer = Car("Chevrolet", "Blazer", 32000, 275, 8)  # Use the named tuple to describe a car<br>chevy_impala = Car("Chevrolet", "Impala", 37495, 305, 5)  # Use the named tuple to describe a different car<br><br>print(chevy_blazer)<br>print(chevy_impala) |
| Car(make="Chevrolet", model="Blazer", price=32000, horsepower=275, seats=8)<br>Car(make="Chevrolet", model="Impala", price=37495, horsepower=305, seats=5)                                                                                                                                                                                                                                                           |
# Dictionary Basics
## Creating a dict
- #dictionary is a python container used to describe associative relationships
- a dict associates keys with values
- #key is a term that can be located in a dictionary
- #value describes some data associated with a key such as a definition 
- a key can be any immutable type
- a tuple can be any type
- dict object is created using curly braces to surround the key:value pairs that comprise the dictionary contents
- `{key:value_pairs}`
- dicts are used in place of lists when an associative relationship exists 
## Accessing dictionary entries
- Dictionaries maintain left-to-right ordering
- entries cannot be accessed through indexing
- key must be specified to access through \[]
- if no matching key is found the program will return *KeyError*
#### Adding modifying and removing dict entries
- Dict is mutable
- new entry is added by using brackets to specify the key:
- Ex:
	- `prices["banana"] = 1.49`
- Dictionary key is unique
- when you create a new entry with a pre-existing key it overwrites the existing entry
- #del is used to remove entries from a dict
- Ex:
	- `del prices["papaya"]` \# removes entry whose key is "papaya"
# Data Structures
**LINK:** [Reading source](https://docs.python.org/3/tutorial/datastructures.html)

## List methods
#list_method 
- list.append(x)
	- add an item to the end of the list
- list.extend(iterable)
	- extend the list by appending all items from the iterable
- list.insert(i, x)
	- Insert an item at a given position
	- first arg is the index of the element before which to insert
- list.remove(x)
	- Remove the first item from the list whose value is equal to x
- list.pop(x)
	- Remove the first item from the list whose value is equal to x
	- raises ValueError if item is not found
- list.clear()
	- Removes all items from a list
- list.index(x\[, start\[, end]])
	- Return zero-based index of the first occurrence of x in the list
	- Returns ValueError if there is no such item
	- Optional args start and end are interpreted as in the slice notation and are used to limit the search to a particular sub sequence of the list. The returned index is computed relative to the beginning of the full sequence rather than the  start arg
- list.count(x)
	- Return the number of times that x appears in the list
- list.sort(\*, key=None, reverse=False)
	- Sort the items of the list in place (the args can be used for sort customization)
- list.reverse()
- list.copy()
	- Return shallow copy. Similar to a\[:]
- del list\[index]
	- This allows you to delete an item based on index as opposed to value 
## List comprehensions
- provide a concise way to create list
- common applications are to make new lists where each element is the result of some operations applied to each member of another sequence or iterable, or to create a sub-sequence for those elements that satisfy a certain condition 
## Tuples and sequences
- lists and strings have many common properties
- such as slicing and indexing operations
- both examples of sequence data type
- Another sequence type is tuple
- #Tuple is another
## Sets
- A #set is an unordered collection with no duplicate elements
- Basic uses include membership testing and eliminating duplicate entries
- Set objects support mathematical operations like union, intersection, difference and symmetric difference
- Curly braces or the set() function can be used to create sets
## Dictionaries 
- Indexed by #keys 
- keys can be any immutable type
	- Strings and nums can always be keys
- keys must be unique
- #dictionary is a collection of key:value pairs
- If you attempt to extract a value for a non existing key value pair you will be met with a *KeyError*
	- To avoid this use get to extract info from dicts
# Searching lists
This is from a free codecamp article that can be referenced [here](https://www.freecodecamp.org/news/python-find-in-list-how-to-find-the-index-of-an-item-or-element-in-a-list/)
- Three techniques used are
- index() list method
- for-loop
- and finally, using list comprehension and enumerate() function
## What are lists? 
- Act as containers that store multiple, typically related, items under the same variable name
- Items are placed and enclosed inside square brackets
- each item in bracket is separated by a comma
- Arrays only store items that are of the same type
- lists are mutable
## Find the Index of an item
- use index()
- `my_list.index(item, start, end)`
- item is the element whose index you are looking for 
- start and end is the range that you are searching for said item
- args are case sensitive
- If there is no match then it will through a ValueError
- index() returns only the first occurrence of an item 