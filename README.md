# Python-Machine-Learning

Created by Vince Chang </br>

All code that pertains to Machine Learning using Python

# Pluralsight Intro Course

# Questions

    1. What is the difference between set and tuple (Other Data Types)
    2. What is a yield generator (Yield)
    3. How do you call a lambda function?

#### Python: Getting Started

- Used for: automations, science, android development, web development (Django)
  , machine learning
- Python uses indentation to represent blocks
- All methods are **_public_**, doesn't have private or protected
- There are **_no interfaces_**
- There is **_no override keyword_**
- There is no `++` operator, but there is `+=` and `-=`
- Integer division is done with `//` Ex. `6//5 == 1`
- `#` Is a comment
- Multi-Line Comments are encapsulated in `""" comment """`
- Code is checked at **_runtime_**

#### Types in Python

- Don't need to define types

#### Strings

- Can use single quotes, double, and triple quotes
- 'Hello World', "Hello World", """"Hello World""""
- String Format Function - "Nice to meet you {0}. I am {1}".format(name,myName) - Use .format when you want to replace like above example - Can also do this `f"Nice to meet you {name}. I am {myName}."`
- `s.lower(), s.upper()` -- returns the lowercase or uppercase version
- `s.strip()` -- returns a string with whitespace removed from the start & end
- `s.isalpha()/s.isdigit()/s.isspace()...` -- tests if all the string chars are
  in the various character classes
- `s.startswith('other'), s.endswith('other')` -- tests if the string starts or
  ends with the given other string
- `s.find('other')` -- searches for the given other string (not a regular
  expression) within s, and returns the first index where it begins or -1 if not
  found
- `s.replace('old', 'new')` -- returns a string where all occurrences of 'old'
  have been replaced by 'new'
- `s.split('delim')` -- returns a list of substrings separated by the given
  delimiter. The delimiter is not a regular expression, it's just text.
  `'aaa,bbb,ccc'.split(',') -> ['aaa', 'bbb', 'ccc']`. As a convenient special
  case `s.split()` (with no arguments) splits on all whitespace chars.
- `s.join(list)` -- opposite of split(), joins the elements in the given list
  together using the string as the delimiter.
  e.g. `'---'.join(['aaa', 'bbb', 'ccc']) -> aaa---bbb---ccc`

#### Boolean and None

- `True` and `False` use **_capitol T and F_**
- `None` is equivalent to `NULL`

#### If Statements

```
number = 5
if number == 5:
	print ("Number is 5")
else:
	print ("Number is NOT 5")
```

- Indentation is important here!
- The colon is also needed!
- `is` is used to know if object is pointing to same place in memory

#### Not If

- Can use `!=` or `if not`
- `and` and `or` is used like && and ||

#### Ternary If Statements

```
a = 1
b = 2
"bigger" if a > b else "smaller"
```

- What prints is smaller because a is smaller than b

#### Lists

- To define a list it will look like this:
  `student_names = ["vince","tracy","sam"]`
- If you want to get the last index you can do `student_names[-1] ,[-2] etc` - `student_names[-1]` == "Sam" and `student_names[-2]` == "tracy"
- .append() -> `student_names.append("ali")` -> ["vince","tracy","sam",ali]
- Find someone in the list: - `"vince" in student_names` will result to `"True"`
- Find the length of the list: - `len(student_names)` will result to 4
- Delete a student: - `del student_names[2]` will delete sam from the list!
- `list.append(elem)` -- adds a single element to the end of the list.
  Common error: does not return the new list, just modifies the original.
- `list.insert(index, elem)` -- inserts the element at the given index,shifting
  elements to the right.
- `list.extend(list2)` adds the elements in list2 to the end of the list. Using

* or += on a list is similar to using extend().

- `list.index(elem)` -- searches for the given element from the start of the
  list and returns its index. Throws a ValueError if the element does not appear
  (use "in" to check without a ValueError).
- `list.remove(elem)` -- searches for the first instance of the given element
  and removes it (throws ValueError if not present)
- `list.sort()` -- sorts the list in place (does not return it). (The sorted()
  function shown below is preferred.)
- `list.reverse()` -- reverses the list in place (does not return it)
- `list.pop(index)` -- removes and returns the element at the given index.
  Returns the rightmost element if index is omitted (roughly the opposite of
  append()).

#### List Slicing

- `student_names[1:]` will give you index 1 until the end (excludes index 0)
- `student_names[1:-1]` this will give you index one, up until index -1 (which
  is the last element in the list) it will be excluded with whatever is returned - student_names = ["vince","tracy","sam"] // initialize - student_names[1:2] will result to tracy - student_names[0:] will print "vince","tracy","sam" // will print to the end

#### For Loop

```
for name in student_names
	print("Student name is {0}.format(name)")
```

- 0 represents the first parameter in the .format function, in this case it
  will be name

```
x = 0
for index in range(10):
	x += 10
	print("The value of X is {0}".format(x))

The value of X is 10
The value of X is 20
The value of X is 30
The value of X is 40
The value of X is 50
The value of X is 60
The value of X is 70
The value of X is 80
The value of X is 90
The value of X is 100
```

- range is used like (start,end) or (start,end,increment)
- ex. - range(5,10) == [5,6,7,8,9] // Note that the last number is always excluded - range(5,10,2) == [5,7,9] // This will increment by 2

#### While Loops

```
x = 0
while x < 10:
	print("Count is {0}.format(x))
	x += 1
```

#### Dictionaries

- This is like Java's Hashmap!
- Looks like .json
- Dictionaries work with Key Value Pairs

```
student = {
	"name" : "Vince",
	"student_id": 123,
	"feedback": None
}
```

- If you need more than one dictionary, need to put it in a List!
  students = [
  {"name": "vince", "student_id": 123},
  {"name": "tracy", "student_id": 456}
  ]

- students.keys() returns ["name","student_id"]
- students.values() returns ["vince", 123, "tracy", 456]
- del students["name"] will delete the key name

```
  ## By default, iterating over a dict iterates over its keys.
  ## Note that the keys are in a random order.
  for key in dict: print key
  ## prints a g o

  ## Exactly the same as above
  for key in dict.keys(): print key

  ## Get the .keys() list:
  print dict.keys()  ## ['a', 'o', 'g']

  ## Likewise, there's a .values() list of values
  print dict.values()  ## ['alpha', 'omega', 'gamma']

  ## Common case -- loop over the keys in sorted order,
  ## accessing each key/value
  for key in sorted(dict.keys()):
    print key, dict[key]

  ## .items() is the dict expressed as (key, value) tuples
  print dict.items()  ##  [('a', 'alpha'), ('o', 'omega'), ('g', 'gamma')]

  ## This loop syntax accesses the whole dict by looping
  ## over the .items() tuple list, accessing one (key, value)
  ## pair on each iteration.
  for k, v in dict.items(): print k, '>', v
  ## a > alpha    o > omega     g > gamma
```

#### Other Data Types

- tuples are similar to lists but are **_immutable (can't change it)_**
- sets order and remove duplicates

#### Functions

- `def functionName():` is how to declare a function
- `*` used in the parameter is optional parameters
- `**` used in parameter is kwargs

#### Opening, Reading & Writing Files

```
def save_file(student):
	try:
		// Open students.txt, a is for append, can have other flags
		f = open("students.txt","a")

		// Writing to the file, \n, is so every student is on a new line
		f = write(student + "\n")

		// Tell OS that we are done writing to the file, prevent memory leaks
		f.close()

	except Exception:
		print("Could not save file")


def read_file(student):
	try:
		// Open students.txt, r is for read
		f = open("students.txt","r")

		for student in f.readlines():
			add_student(student)

		// Tell OS that we are done writing to the file, prevent memory leaks
		f.close()

	except Exception:
		print("Could not read file")
```

#### Lambda Functions

- Lambda functions don't use the `def` keyword
- Ex. We have a number and multiply it by 2

```
def double(x):
	return x*2
```

`double = lambda x: x*2`

- Lambda functions are useful when using functions within functions

#### Defining Classes

- Don't need to write code inside a class like Java, you can, but only if you
  want to
- A class is a logical group of data
- ex. `class Student:`
- Each student I make is independent of the other Students that I create

```
students[]
class Student:
	// Using self is like this in java
	def add_student(self,name,student_id = 332):
		student = {"name": name, "student_id": student_id}
		students.append(self)

// Creating a new instance of Student, both are stored in different locations
student = Student()
student.add_student("vince") // will give "vince" default student id of 332


// Can do the above with using the default constructor instead of calling
// add_student
students[]
class Student:
	def __init__(self,name,student_id = 332): // Using a constructor!
		student = {"name": name, "student_id": student_id}
		students.append(self)

	// __str__ overrides the __init__ function!
	def __str__(self):
		return "Student"


student = Student("vince")
```

#### Class and Instance Attributes

```
students[]
class Student:

	school_name = "Thomas Edison Elementary"


	def __init__(self,name,student_id = 332): // Using a constructor!
		self.name = name
		self.student_id = student_id
		students.append(self)

	// __str__ overrides the __init__ function!
	def __str__(self)
		return "Student " + self.name

	def get_name_capitalize(self)
		return self.name.capitalize()

	def get_school_name(self)
		return self.school_name

//student = Student("vince")
//print(student)

// Call this static with the class name, don't need the object to use this!
print(Student.school_name)
```

#### Inheritance and Polymorphism

```
students[]
class Student:

	school_name = "Thomas Edison Elementary"


	def __init__(self,name,student_id = 332): // Using a constructor!
		self.name = name
		self.student_id = student_id
		students.append(self)

	// __str__ overrides the __init__ function!
	def __str__(self)
		return "Student " + self.name

	def get_name_capitalize(self)
		return self.name.capitalize()

	def get_school_name(self)
		return self.school_name

// The derived class is the HighSchoolStudent and the parent class is the
// Student class. HighSchoolStudent has access to methods in Student Class
class HighSchoolStudent(Student):
	school_name = "Westmoor High School"


	def get_school_name(self):
		return "This is method overrides the other get_school_name from Student"

	// Uses the method from Student but also adds more to it
	def get_name_capitalize(self):
		original_value = super().get_name_capitalize()
		return original_value + -"HS"

vince = HighSchoolStudent("vince")
print(vince.get_name_capitalize()); // Will return "Vince -HS" still works!
print(vince.get_school_name) // Will return HighSchoolStudent's method
```

#### Using a Main.py

- From above code examples, just split Student code in student.py and
  HighSchoolStudent code in highschoolstudent.py
- import the classes into main - `from student import *` // this means that import everything from
  this student.py!

#### Virtual Environments

- Allows you to set up environments
- You can switch from version to version without conflict
- So you can make 2 isolated environments and still be on the same machine
- Common to have multiple VM's for different applications

#### Debugging Python Code

- Use **_breakpoints_** with the IDE can use PyCharm to set breakpoints

#### Regular Expressions

- Uses the `re` module
- ex. `match = re.search(pat,str)`
- `re.search()` method takes a regex pattern and a string and searches for that
  pattern within the string
- If the search was successful, search returns a match object or None otherwise
- Therefore, the search statement is usually immediately followed by an
  if-statement to test if the search was successful

```
str = 'an example word:cat!!'
match = re.search(r'word:\w\w\w', str) # The r is needed to pass in \ with np!
# If-statement after search() tests if it succeeded
  if match:
    print 'found', match.group() ## 'found word:cat', result is stored in match
  else:
    print 'did not find'
```

#### Basic Regex Patterns

- `a, X, 9,` < -- ordinary characters just match themselves exactly. The
  meta-characters which do not match themselves because they have special
  meanings are: . ^ \$ \* + ? { [ ] \ | ( ) (details below)
- `.` (a period) -- matches any single character except newline '\n'
- `\w` -- (lowercase w) matches a "word" character: a letter or digit or
  underbar [a-zA-Z0-9_]. Note that although "word" is the mnemonic for this, it
  only matches a single word char, not a whole word.
- `\W` (upper case W) matches any non-word character.
- `\b` -- boundary between word and non-word
- `\s` -- (lowercase s) matches a single whitespace character -- space, newline
  return, tab, form [ \n\r\t\f].
- `\S` (upper case S) matches any non-whitespace character.
- `\t, \n, \r` -- tab, newline, return
- `\d` -- decimal digit [0-9] (some older regex utilities do not support but
  \d, but they all support \w and \s)
- `^ = start, $ = end` -- match the start or end of the string
- `\` -- inhibit the "specialness" of a character. So, for example, use `\`.
  to match a period or `\\` to match a slash. If you are unsure if a character
  has special meaning, such as '@', you can put a slash in front of it, `\@`, to
  make sure it is treated just as a character.

```
  ## i+ = one or more i's, as many as possible.
  match = re.search(r'pi+', 'piiig') =>  found, match.group() == "piii"

  ## Finds the first/leftmost solution, and within it drives the +
  ## as far as possible (aka 'leftmost and largest').
  ## In this example, note that it does not get to the second set of i's.
  match = re.search(r'i+', 'piigiiii') =>  found, match.group() == "ii"

  ## \s* = zero or more whitespace chars
  ## Here look for 3 digits, possibly separated by whitespace.
  match = re.search(r'\d\s*\d\s*\d', 'xx1 2   3xx') =>  found, match.group() == "1 2   3"
  match = re.search(r'\d\s*\d\s*\d', 'xx12  3xx') =>  found, match.group() == "12  3"
  match = re.search(r'\d\s*\d\s*\d', 'xx123xx') =>  found, match.group() == "123"

  ## ^ = matches the start of string, so this fails:
  match = re.search(r'^b\w+', 'foobar') =>  not found, match == None
  ## but without the ^ it succeeds:
  match = re.search(r'b\w+', 'foobar') =>  found, match.group() == "bar"
```
