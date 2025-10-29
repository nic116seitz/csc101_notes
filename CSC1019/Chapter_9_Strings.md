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

| Example                           | Expression result | Why?                                                                                                                                                                                               |
| --------------------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `"Hello" == "Hello"`              | True              | The strings are exactly identical values                                                                                                                                                           |
| `"Hello" == "Hello!"`             | False             | The left hand string does not end with "!".                                                                                                                                                        |
| `"Yankee Sierra" > "Amy Wise"`    | True              | The first character of the left side "Y" is "greater than" (in ASCII value) the first character of the right side "A".                                                                             |
| `"Yankee Sierra" > "Yankee Zulu"` | False             | The characters of both sides match until the second word. The first character of the second word on the left "S" is not "greater than" (in ASCII value) the first character on the right side "Z". |
| `"seph" in "Joseph"`              | True              | The substring "seph" can be found starting at the 3rd position of "Joseph".                                                                                                                        |
| `"jo" in "Joseph"`                | False             | "jo" (with a lowercase "j") is not in "Joseph" (with an uppercase "J").                                                                                                                            |
- for <> comparison the result will be the result of comparing the ASCII/Unicode of the first differing character pair
- If all matching pairs are the same the one that has less characters is considered smaller
- Identity operators determine whether the two arguments are bound to the same object. 
- Good practice is to use equality operator when comparing values

Methods to check a string value that returns a True or False Boolean value:

- isalnum() -- Returns True if all characters in the string are lowercase or uppercase letters, or the numbers 0-9.
- isdigit() -- Returns True if all characters are the numbers 0-9.
- islower() -- Returns True if all cased characters are lowercase letters.
- isupper() -- Returns True if all cased characters are uppercase letters.
- isspace() -- Returns True if all characters are whitespace.
- startswith(x) -- Returns True if the string starts with x.
- endswith(x) -- Returns True if the string ends with x.

#new_string_methods 
Methods to create new strings:

- capitalize() -- Returns a copy of the string with the first character capitalized and the rest lowercased.
- lower() -- Returns a copy of the string with all characters lowercased.
- upper() -- Returns a copy of the string with all characters uppercased.
- strip() -- Returns a copy of the string with leading and trailing whitespace removed.
- title() -- Returns a copy of the string as a title, with first letters of words capitalized.
*Transformation should be applied after taking input, as this lowers the risk of something going wrong*

# Splitting and joining strings
## The split() method
- split() splits a string into a list of tokens
- each #token is a substring that forms a part of a larger string
- #seperator is a char or sequence of chars that indicates where to split the string into tokens
- Ex:
 ```
 string = "This/That/Theother"
 my_tokens = string.split("/")
 ```
 `Output: my_tokens = ["This","That","Theother"]`
## The join() method
- performs the inverse of split()
- joins a list of strings to create a single string 
- useful way to use this is "".join to add things together without space
# String basics
## Strings and string literals
- a #string is a sequence of char that represents textual data like a person's name, location or a message to the user
- #string_literal is a string defined in the source code of the program by surrounding the text value with single or double quotes
- a string is a #sequence_type a type that orders a collection of objects into a sequence from first to last 
- empty string is `var = ""`
- len() can be used to find the length of a string
- A programmer can reference a char at a specific index by appending #brackets \[] containing the desired index after the name of a string variable
- Strings are immutable
- a string variable cannot change once created
- assignment statement must be used to create a new string object to replace the old one 
- strings can be concatenated
- EX:
- `"New" + "York" = "New York"`

# String formatting
## Formatted string literals (f-strings)
- #fstring starts with a f before opening quote and uses \{} to denote place holder expressions
- these expressions are also called a #replacement_field
- `=` after the expression in the replacement field prints both the expression and its result
- `{{}}` creates the output wrapped in `{}`
##### Format specifications
- #format_specification inside a replacement field allows a value's formatting in the string to be customized
- `:` is what denotes this 
- it separates the what from the how 
- #presentation_type is a part of a format spec that determines how to represent a value in text form  

## Questions
- How do you slice from the end of a string?
- When should you apply string transformations to something?
- 
