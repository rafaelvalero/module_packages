# module_packages
Tutorial about classes, modules and packages in Python
For more details check the wiki: https://github.com/rafaelvalero/module_packages/wiki



# **Creation of modules and packages**

# Table of contents
1. [Introduction](#introduction)
2. [Difference between module and packages](#Difference_between_module_and_packages)
    1. [Take away](#take_away)
2. [Further Thoughts](#Further_Thoughts)
3. [References](#References)

# Introduction <a name="introduction"></a>
How to distinguish between modules and packages in Python, largely based on https://www.youtube.com/watch?v=aJeb1j_dlOA&t=185s.

## Difference between module and packages <a name="Difference_between_module_and_packages"></a>

A module is a single file (or files) that are imported under one import and used. e.g.
`import my_module`
A package is a collection of modules in directories that give a package hierarchy.
`from my_package.timing.danger.internets import function_of_love`



### Take away <a name="take_away"></a>
Packages are a way of structuring Python’s module namespace by using “dotted module names”. For example, the module name A.B designates a submodule named B in a package named A
Packages are a way of structuring Python's module namespace by using "dotted module names". For example, the module name ‘A.B’ designates a submodule named ‘B’ in a package named ‘A’. Just like the use of modules saves the authors of different modules from having to worry about each other's global variable names, the use of dotted module names saves the authors of multi-module packages like NumPy or the Python Imaging Library from having to worry about each other's module names.

### References about differenciation between packages and module
* https://stackoverflow.com/questions/7948494/whats-the-difference-between-a-python-module-and-a-python-package

# Example of file
see https://github.com/rafaelvalero/module_packages/blob/master/file_example.py
```
def sayHello(name):
    print 'My name is '+ name
```

# Example of module
see https://github.com/rafaelvalero/module_packages/blob/master/file_example_module.py
Molue code:

Script to call the module:
```
from module_1 import person

person_1 = person()
person_1.name = 'Computer'
person_1.sayHello()
```

# Example of package
https://github.com/rafaelvalero/module_packages/blob/master/file_example_package.py
The package has the next structure:
```
my_package/
    __initi__.pyc
    Car.py
```

The package has two files in a separated folder called "my_package". One file called __init__.pyc to initiallice the package, to see more about '__init__.py' click [here](http://mikegrouchy.com/blog/2012/05/be-pythonic-__init__py.html).

Scrip to call the package (and module):
```
from module_1 import person`



person_1 = person()
person_1.name = 'Computer'
person_1.sayHello()





from my_package.Car import Car,Truck

my_car= Car()
my_car.setSpeed(100)


my_truck= Truck()
my_truck.setSpeed(90)
```



# Interesting future topics  <a name="Further_Thoughts"></a>
1. The role of `__init__`, `__self__`, .pyc ...

# References <a name="References"></a>


## About differenciation between packages and module
* With examples and learning by doing: https://www.learnpython.org/en/Modules_and_Packages
* https://stackoverflow.com/questions/7948494/whats-the-difference-between-a-python-module-and-a-python-package


## Videos tutorials
* **Excellent tutorial comparing both, modules and packages**: https://www.youtube.com/watch?v=aJeb1j_dlOA&t=185s
* Creation of module: https://www.youtube.com/watch?v=xRQA1Fy1HFQ
* Creation of package: https://www.youtube.com/watch?v=qmsTqQbcBNM


# How to create good repositories
* Structure of the repositories/project:

  * https://airbrake.io/blog/python/python-best-practices
  * http://docs.python-guide.org/en/latest/writing/structure/
* How to write some of the documentation:
http://docs.python-guide.org/en/latest/writing/documentation/
