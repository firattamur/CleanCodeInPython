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

<h3>
	Chapter - 3: Functions
</h3><hr>

<h3>
	References:
</h3><hr>

1. [Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
