# Object Oriented Programming(Python)
---
Object Oriented programming is a widely used concept to write powerful applications. OOP uses the concept of objects and classes. The concept of object-oriented programming in python focuses on creating reusable code.
### Class: 
---
 A class is a blueprint for the object.
### Object:
---
An object is an entity that possesses both state (or properties or attributes) and behavior. The data is usually hidden from other objects so that the only way to affect the data is through the object’s functions. 

An object has two characteristics:
    •	Attributes
    •	Behavior
    
An example of an object is a car. A car has attributes name, color, size, weight, type etc., and has behavior stop, accelerate, turn on wipers etc.

In Python, the concept of OOP follows some basic principles:

#### Inheritance: 
The transfer of the characteristics of a class to other classes that are derived from it.
#### Encapsulation: 
Hiding the private details of a class from other objects.
#### Polymorphism:
A concept of using common operation in different ways for different data input.

### Example:

Suppose we have details of name, age and salary of an employee . The below program shows how to build the class and objects of employee. 
```
class employee:
    def __init__(self, name, age, salary ):
        self.name = name
        self.age = age
        self.salary = salary
        
    def introduce_self(self):
        print("name of the employee is " + self.name)

    def Employee_data(self):
        print("Name : ",self.name, ", Age: ",self.age, ", Salary: ",self.salary)
        
e1 = employee("ajay", 24, 45040)
e2 = employee("ram", 26, 54989)

e2.introduce_self()
Employee_data(e1)
```
### Output:
```
name of the employee is ram
Name :  ajay , Age:  24 , Salary:  45040
```
