## String slicing basics
- Strings are a sequence type
- Have char that are indexed right to left
- #slice_notation can be used to read multiple characters at at time
- Syntax:
	- `my_str[start:end]`
- lists and tuples support slice notation
- last char is one location before the end (4 would be the fourth letter in a word) 
- negative numbers are used to count from the end
## Slicing and slicing operations
- new object is created by slicing
- common slicing operations:


| Syntax          | Result                            | Description                                                           |
| --------------- | --------------------------------- | --------------------------------------------------------------------- |
| `my_str[10:19]` | wikipedia                         | Returns the characters in indices 10-18.                              |
| `my_str[10:-5]` | wikipedia.org/wiki/               | Returns the characters in indices 10-28.                              |
| `my_str[8:]`    | n.wikipedia.org/wiki/Nasa/        | Returns all characters from index 8 until the end of the string.      |
| `my_str[:23]`   | http://en.wikipedia.org           | Returns every character up to index 23, but not including my_str[23]. |
| `my_str[:-1]`   | http://en.wikipedia.org/wiki/Nasa | Returns all but the last character.                                   |

## The slice stride
- #stride determines how much to increment the index after reading each element


# Advanced string formatting

## Field width
- A format specification may include a #field_width
- this defines the minimum number of chars that must be inserted into the string
- if the replacement is less then the #field_width the string is padded with space characters
- The formatting for this is below:
	  `x = desired_field_width`
		`print(f"{'variable':x}`
## Text alignment
- format spec can also include an #alignment_character 
- determines how a value should be aligned in width of fields
- Basic set of possible alignment are `< ^ >` 
- these stand for left right and center
## Fill
- A #fill_character is used to pad a replacement field when the inserted string is smaller than the field width
- the default is " " this can be changed by changing the character before alignment
	- `{variable:0>4} generates 0009 if score = 9` 
## Floating point precision
- This is the syntax explanation for how to program an f string to print a certain number of places
- Syntax
```
x = 1 # desired number of digits to the right of the floating point 
var = 3.14
print(f"{var:.xf}") # basic syntax for floating point precision

Output:
3.1
  
  ```
# Str methods
## Find and replace
- #replace 
- `replace(old, new)` - returns a copy of the string with all the occurrences of `old` replaced by `new`
- `replace(old, new, count)` - same as above but only for the amount of times specified in count
- #function_definition 
- `find(x)` - Returns the index of first occurrence of x otherwise returns -1. x may be a string variable or string literal
- `find(x, start)` - does the same as above but starts at specified index
- `find(x, start, end)` - does the same as above but ends at the specified end index
- `rfind(x)` - same as find but searches in reverse returning last occurrence 
- `count(x)` - returns the amount of times x occurs in string
## String Comparison 
## Questions
- How do you slice from the end of a string?
- 
