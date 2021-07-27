<h3 align="center">
Clean Code in Python
</h3>

<!-- badges -->
<p align="center">

<!-- language -->
<img src="https://img.shields.io/badge/python-3.6-blue.svg" alt="Python: 3.6">

<!-- inprogress or completed -->
<!-- <img src="https://img.shields.io/badge/-completed-green" alt="completed"> -->

<!-- inprogress or completed -->
<img src="https://img.shields.io/badge/-in%20progress-red" alt="in progress">
	
<!-- licence -->
<a href="https://github.com/ftamur/iOSPencilKitDrawApp/blob/main/LICENSE">
<img src="https://img.shields.io/badge/License-MIT-lightgrey.svg" alt="License: MIT">
</a>

<!-- week of year -->
<img src="https://img.shields.io/badge/week-29-green" alt="in progress">
	
</p>

<div align="center">
	<img src="https://mk0osnewswb2dmu4h0a.kinstacdn.com/images/comics/wtfm.jpg"></img>
</div>


<h4 align="center">
	Short Notes and Examples from Clean Code Book in Python
</h4><hr>

<h3>
	Goals:
</h3>

- [ ] Complete Clean Code book in a week.
- [ ] Understand content and write examples in Python.

<hr>

<h3 align="center">
	Clean Code:
</h3>

<h3>
	Chapter - 1: Clean Code
</h3><hr>

* There will always be code!
* Bad code can bring down a successful app!
* Rushing to code usually ends up with bad code!
* Later means never. Instead of rushing to code, write clean code at the beginning!
* Without clean code, productivity decreases, and complexity of program increases over time!
* Write clean code even with a limited schedule. Defend the code! 
* Acquire "code-sense". Programmers with "code-sense" see options and alternatives when they encounter messy code. 
* "The logic should be straightforward to make it hard for bugs to hide.", **Bjarne Stroustrup**
* "Clean code does one thing well!",  **Bjarne Stroustrup**
* Bad code tries to do too much!
* "Clean code reads like well-written prose!", **Grady Booch**
* "Clean code can be read, and enhanced by a developer other than its original author. It has unit and acceptance tests.", **Dave Thomas**
* "Clean code always looks like it was written by someone who cares.", **Michael Feathers**

<h3>
	Chapter - 2: Meaningful Names
</h3><hr>

* Use intention-revealing names. If a variable need comments to explain its purpose then it doesn't have a good name!
* Change names when you find a better one!
```python
# bad code:
c = 0 # counter to keep number of passengers

# clean code:
passengerCount = 0
```

* Use informative names!

```python
# bad code:
theList = list()

# clean code:
passengers = list()
```

* Avoid disinformation! 

```python
# Do not use List in a name if it is not actually a member of List datatype. 
# bad code:
passengerList = set()

# clean code:
passengersSet = set()
```

* Do not use very similar names! You may use wrong name if you use autocomplete in your IDE. 

```python
# bad code:
def getDataFromAPIAndCreateUser():
    pass

def getDataFromAPIAndCreateUsers():
    pass

# clean code:
def getDataFromAPIAndCreateSingleUser():
    pass

def getDataFromAPIAndCreateMultipleUsers():
    pass
```

* Do not use single letters which look very similar digits. 

```python
# bad code:
# letter 'l' very similar to digit '1'
# letter 'O' very similar to digit 0
for l, O in enumerate(passengers):
    print(l, O)

# clean code:
for i, p in enumerate(passengers):
    print(i, p)
```

* Make meaningful distinctions. Number series naming is wrong type of naming. 

```python
# bad code:
def clone(a1, a2):
    pass

# clean code:
def clone(source, destination):
    pass
```

* Noise words are redundant. For example, the **variable** word should never appear in a variable name. 

```python
# bad code:
counterVariable = 0
nameString = "python"

# clean code:
counter = 0
name = "python"
```

* Programming is a social activity. So make your names pronounceable!

```python
from datetime import date

# bad code:
genymdhms = date.today() # generation date, year, month, day, hour, minute, and second.

# clean code:
generationTimeStamp = date.today()
```

* Use searchable names! Single-letter names and numeric constants may be problem when you need to search them in the code. 

```python
# bad code:
# here letters n, m may be in many lines 
# also numeric constants 10, 10000 may be hard to find when seach in the code. 
n = 10 
m = 10000

# clean code:
numberOfStudents = INITIAL_NUMBER_OF_STUDENTS
maxNumberOfStudents = MAX_NUMBER_OF_STUDENTS
```

* Single-letter names should be used only as local variables inside short methods. 
* The length of a name should correspond to the size of its scope. 
* Avoid mental mapping. Single-letter names for loop counters like i, j, and k are traditional and there is no problem to use them if scope is small and there is no other name conflict with them. 
* The difference between smart programmer and professional one is that the professional understands that **clarity is king**.
* Class and objects should have noun or noun phrase names like Customer, WikiPage, Account. Avoid words like Manager, Processor and Data. 
* A class name should not be a verb!
* If a constructor of a class overloaded, use static factory methods with names that describe the arguments. 

```python
# bad code:
jsonParser = DataParser(JSONObject)
xmlParser = DataParser(XMLObject)

# clean code:
jsonParser = DataParser.parserForJSON(JSONArgs)
xmlParser = DataParser.parserForXML(XMLArgs)
```

* Don't try to be cute. **Say what you mean. Mean what you say!**

```python
# bad code:
passengerList.HolyHandGrenade() # it's cute but who needs it. 

# clean code:
passengerList.deleteAllItems()
```

* Pick one word and for one abstract concept and stick with it. It will be confusing using different words for same methods in difference classes. For example, **fetch**, **retrieve** and **get** all mean same thing, but do not use all together in your code!

* Most of time the people who read your code will be programmers. So you can use computer science terms in your naming. 
* Shorter names are generally better than longer ones, so long as they are clear. 

<h3>
	Chapter - 3: Functions
</h3><hr>

- **Small!!!** The most important rule for functions is that functions must be small!
- Functions should hardly ever be 20 lines long!
- The indent level of function should not be greater than one or two!
- **Do One Thing**. Functions should do one thing. They should do it well, they should do it only!
- All statements in a function must have **same level of abstraction**!
- Following **The Stepdown Rule** helps to keep abstraction level consistent!
- If you can divide a function to sections, that function does more than one thing!
- **Switch Statements**

<h3>
	References:
</h3><hr>

1. [Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
