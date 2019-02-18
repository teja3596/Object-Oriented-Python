# Object Oriented Python
---
Object Oriented programming is a widely used concept to write powerful applications. OOP uses the concept of objects and classes. The concept of object-oriented programming in python focuses on creating reusable code.  
## Class: 
 A class is a blueprint for the object.
## Object:
An object is an entity that possesses both state (or properties or attributes) and behavior. The data is usually hidden from other objects so that the only way to affect the data is through the object’s functions.
### Example:
```
	class A:
    	def function1():
        	print("function1 is working")
    	def function2():
        	print("function2 is working")
        
     	A.function1()       
     	A.function2()
```
### Output:
```
	function1 is working
	function2 is working
```
### Practical Example:
Suppose we have details of name, age and salary of an employee . The below program shows how to build the class and objects of employee. 
#### Program:
```
class employee:
    def __init__(self, name, age, salary ):
        self.name = name
        self.age = age
        self.salary = salary
        
    def introduce_self(self):
        print("name of the employee is " + self.name)

    def Employee_data(self):
        print("Name : ",self.name, ", Age: ",self.age, ", Salary:     
              ",self.salary)

e1 = employee("ajay", 24, 45040)
e2 = employee("ram", 26, 54989)

e2.introduce_self()
e1.Employee_data()
```
### Output:
```
name of the employee is ram
Name :  ajay , Age:  24 , Salary:  45040
```
In the above program, we create a class with name employee. Then, we define the attributes names, age and salary of an object.
	
## Inheritance:
---
Inheritance provides code reusability to the program that is we can use an existing class to create a new class instead of creating it from scratch. In inheritance, the child class acquires the properties and can access all the data members and functions defined in the parent class. A child class can also provide its specific implementation to the functions of the parent class.

In Python, the concept of Inheritance is classified in to three types:

     •	Single level Inheritance
     •	Multi-level Inheritance
     •	Multiple Inheritance

## Example for single level Inheritance:
```
	class A:
    		def function1():
        		print("function1 is working")
    		def function2():
        		print("function2 is working")
	class B(A):
		    def function3():
			    print("function3 is working")
    		def function4():
        		print("function4 is working")

	B.function1()
	B.function3()
```
### Output:
```
    function1 is working
    function3 is working
```
In the above program, we created two classes A(parent class) and B(child class). B is the child class or subset of A such that b is inheriting the features from A.

### Multi-level Inheritance:
---
In multi-level inheritance, the features of all the base classes are inherited into the derived class. 
### Example:
```
	class A:
    		def function1():
        		print("function1 is working")
    		def function2():
        		print("function2 is working")

	class B(A):
    		def function3():
        		print("function3 is working")
    		def function4():
        		print("function4 is working")
     	class C(B):
   		def function5():
        		print("function5 is working")

	C.function1()       
	C.function4()
	C.function5()
```
### Output:
```
      function1 is working
      function4 is working
      function5 is working
```
In the above program, we have three classes A, B and C, where A is the super class, B is its sub(child) class and C is the sub class of B. The sub(child) class C can access both sub class B and the super class A.
### Practical Example:
Let us consider three classes employee, paying and salary which takes name, age, gender and basic pay as input and it gives the result total salary by calculating basic pay, HRA and DA. The program as follows:


#### Program:
```
class employee:
    def emp(self):
        self.name = input('Name: ')
        self.age = input('Age: ')
        self.gender = input('Gender: ')
        
class paying(employee):
    def pay(self):
        self.basic = int(input('Basic Pay: '))
        self.hra = self.basic*0.40
        self.da = self.basic*0.14

class salary(paying):
    def display(self):
        print('\nName: ',self.name)
        print('Age: ',self.age)
        print('Gender: ',self.gender)
        print('salary: ',self.basic+self.hra+self.da)

s = salary()
s.emp()
s.pay()

s.display()
```
### Output:
```
Name: John
Age: 33
Gender: Male
Basic Pay: 80000

Name:  John
Age:  33
Gender:  Male
salary:  123200.0
```
## Multiple Inheritance:
---
In multiple inheritance, an object or class can inherit characteristics and features from more than one parent object or parent class.
### Example:
In the below program we have three classes A, B and C. Here, b is not inheriting the features from A. However, C is inheriting the features from A and B.
	
```
class A:
    def function1():
        print("function1 is working")
    def function2():
        print("function2 is working")

class B:
    def function3():
        print("function3 is working")
    def function4():
        print("function4 is working")
        
class C(A,B):
    def function5():
        print("function5 is working")
```
### Program:
```
class Calculation1:  
    def Summation(self,a,b):  
        return a+b;
    
class Calculation2:  
    def Multiplication(self,a,b):  
        return a*b;
    
class Derived(Calculation1,Calculation2):  
    def Divide(self,a,b):  
        return a/b;
    
d = Derived()  
print("The sum of a and b is",d.Summation(10,20))
print("The multiplication of a and b is",d.Multiplication(10,20))  
print("The division of a and b is",d.Divide(10,20))
```
### Output:
```
The sum of a and b is 30
The multiplication of a and b is 200
The division of a and b is 0.5
```
















