# Class Inheritance

We demonstrate inheritance in a very simple example. We create a Person class with the two attributes "firstname" and "lastname". This class has only one method, the Name method, essentially a getter, but we don't have an attribute name. This method is a further example for a "getter", which creates an output by creating it from more than one private attribute. Name returns the concatenation of the first name and the last name of a person, separated by a space. It goes without saying that a useful person class would have additional attributes and further methods. 

This chapter of our tutorial is about inheritance, so we need a class, which inherits from Person. So far employees are Persons in companies, even though they may not be treated as such in some firms. If we created an Employee class without inheriting from Person, we would have to define all the attributes and methods in the Employee class again. This means we would create a design and maybe even a data redundancy. With this in mind, we have to let Employee inherit from Person.

The syntax for a subclass definition looks like this:


```python
class DerivedClassName(BaseClassName):
    pass
```

Of course, usually we will have an indented block with the class attributes and methods instead of merely a pass statement. The name BaseClassName must be defined in a scope containing the derived class definition. With all this said, we can implement our Person and Employee class: 

```python
class Person:

    def __init__(self, first, last):
        self.firstname = first
        self.lastname = last

    def Name(self):
        return self.firstname + " " + self.lastname

class Employee(Person):

    def __init__(self, first, last, staffnum):
        Person.__init__(self,first, last)
        self.staffnumber = staffnum

    def GetEmployee(self):
        return self.Name() + ", " +  self.staffnumber

x = Person("Marge", "Simpson")
y = Employee("Homer", "Simpson", "1007")
```

Our program returns the following output: 

```bash
$ python person.py 
Marge Simpson
Homer Simpson, 1007
```

The `__init__` method of our Employee class explicitly invokes the `__init__method` of the Person class. We could have used super instead. `super().__init__(first, last)` is automatically replaced by a call to the superclasses method, in this case `__init__`:

````python
  def __init__(self, first, last, staffnum):
        super().__init__(first, last)
        self.staffnumber = staffnum
````