# Object Oriented Programming

Object Oriented programming (OOP) is a programming paradigm that is based on the concept of classes and objects. In procedure oriented programming languages we see a program as series of instructions where as object oriented pattern views it as a group of objects that have certain properties and can take certain actions. This way of handling the problem makes a code reusable and easy to understand the workflow. There are many programming languages that adopts this paradigm for example : C++, Java and Python.

<b>Note* </b> C++ is not purely object oriented, JAVA is a purely object oriented programming language

we are going to understand what are the basic building blocks of OOP.
* Class
* Objects
* Attributes
* Methods

### <b>Class </b>:
class is similar to strcture in C just the difference is that we can specify what things must hidden and what things must be open for access through out the code. class is a way of binding data and functions together. We can say class is a template code which holds information and procedures in it and we can create objects from this templates.

The general form of class declaration is:
``` cpp
class class_name
{
    private:
	    variable1
	    function1;
	
    public :
	    variable2;
	    function2;
};
```

### <b>Objects </b> :
once class has been created we can create instance of this class type this is nothing but the object or in simple words we can say object is variables of type class.  We can have more than one object for a class. We can create object of class by specifying class name followed by object name we want to create. As we know class is just a template so it will not have any memory allocation untill an object is created. Below is the syntax for creating objects of a class.

```cpp

class_name   object_name;

```

### <b>Attributes </b> :
Attributes are the information or data or variables that are defined inside a class.

### <b>Methods </b> :
Particular group of tasks mentioned inside the class is named as Method. It is nothing but a function in any other programming language. We can asses methods using object of the class.

Below code snippet shows the basic syntax of class

```cpp
class Home
{
    private:
	    char name[20]; //Attribute
	    int FlatNum; //Attribute
    public:
	    void getdetails(){} //Method
};

int main()
{
Home obj1; // obj1 is a object
}

```

## Principles of OOP
Object-oriented programming has four basic Principles as mentioned follows.

1. Encapsulation
2. Abstraction
3. Polymorphism
4. Inheritence
 
<div style='text-align:center'><img src="https://static.studytonight.com/cpp/images/oops-concept-basic-cpp.png" style="background-color:white"></div>

## <b>1. Encapsulation</b>
Binding Attributes and Methods together is called as encapsulation.
along with variables and functions a class have two main types of parameters these are constructors and destructors we can see a little bit about them in  below section.

### Constructors and Destructors of a class

#### a) default Constructors:

A constructor is a special member function inside the class whose task is to initialize the objects of its class. It's name is same as the name of the class.
The constructor is invoked whenever an object of it's associated class  is created.<br />
It is called constructor because it constructs the values of data members of the class. constructor name is same as that of class name.

<br />**Example**

```cpp
class add
{
    int X,Y;
  public:
    add (void)
    {
        X=0;
        Y=0;
    };
};

int main()
{
    add obj1;
}
```

#### b) Parameterized Constructors

When a constructor is parametrized, we must pass the initial values as arguements to the constructor function.

<br />**Example**

```cpp
class add
{
    int X,Y;
  public:
    add (void)  //default constructor
    {
        X=0;
        Y=0;
    };
    add (int value1,int value2)  //parameterised constructor
    {
        this->X=value1;
        this->Y=value2;
    };
};

int main()
{
    add obj1;
    add obj2(20,5);
}
```
#### c) Copy Constructor

A copy constructor takes object as a parameter of same class.

<br />**Example**
```cpp
class add
{
    int X,Y;
  public:
    add (void)  //default constructor
    {
        X=0;
        Y=0;
    };
    add (int value1,int value2)  //parameterised constructor
    {
        this->X=value1;
        this->Y=value2;
    };
    add (add &ref)  //copy constructor
    {
        this->X=ref.X;
        this->Y=ref.Y;
    }
};

int main()
{
    add obj1;
    add obj2(20,5);
    add obj3(obj2);
}
```

## Destructor
Destructor is used to deallocate the resources
and destroy the objects that have been created by a constructor. There can be only one destructor in our class. Destructor never takes any arguements nor returns any value It will be invoked implicitly by the compiler upon exit from the object.
For markdown syntaxDistructor will also have same name as of class name just the difference between syntax of constructor and distructor is distructor name will start with tilda (~).

<br />**Example**

```cpp
class add
{
    int X,Y;
  public
    add (:void)  //default constructor
    {
        X=0;
        Y=0;
    };
    ~add(void) //Destructor
    {
        cout<<"Inside destructor\n";
    }
};

int main()
{
    add obj1;   //Object
}
```

---
## <b>2. Abstraction</b>
Hiding some things from outside world is known as abstraction. we can achieve abstraction using various access specifiers in OOPS

The concept of access specifiers is used to indicate who can access members of a class. There are three types of access specifiers

* Public:
  
  The members which are written under public access specifier are accessible to everyone.

* Private :

  The members which are written under private access specifier are not accessible anyone except that of class members.
  Using private we can achieve 100% abstraction.

* Protected :

  The members which are written under protected access specifier are accessible to its immidiate derived class. we can achieve partial abstraction.

---

## <b>3. Polymorphism</b>
 Single name and multiple behaviours is known as Polymorphism. In other words i can say that "looking alike but exhibit different characteristics".

In C++, polymorphism can be either
1. Compile time polymorphism (static)(Overloading)
2. Run time polymorphism(dynamic)(Overriding)

![image](https://media.geeksforgeeks.org/wp-content/uploads/20200703160531/Polymorphism-in-CPP.png)

You can refere following URL for more information on Polymorphism
[**click here**](https://www.geeksforgeeks.org/polymorphism-in-c/?ref=lbp)

---

## <b>4.  Inheritance</b>

Inheritance means deriving qualities and characteristics from parents or ancestors. 

Inheritance in Object Oriented Programming can be described as a process of creating new classes from existing classes which will have the properties similar to that of parent classes.
Or simply, Inheritance is the process by which objects of one class acquire the properties of objects of another class in the hierarchy.

Derived class provide specialized behavior from the basis of common elements provided by the Base class. Through the use of inheritance, programmers can reuse the code in the Base class many times.

Reusing existing code saves time and money and increases a program’s reliability.

![image](https://user-images.githubusercontent.com/26179770/36838639-b9c269e4-1d65-11e8-9c98-506477719a4d.png)

New classes can be built from the existing classes. It means that we can add additional features to an existing class without modifying it. The new class is referred as derived class or subclass and the original class is known as base classes or super class.

In below example caluculator class is derived from math class so that calculator will have access to all the methods such as add, sub which are present in math class under public access also it is having its own behavior that is mult function extra.

<br />**Example**

```cpp
#include<iostream.h>
using namespace std;

class Math
{
    public:
        int x,y;

        int add(int no1,int no2)
        {
            return no1+no2;
        }

        int sub(int no1,int no2)
        {
            return no1-no2;
        }
}

class Calculator:public Math
{
    public:
        int z;
        int mult(int no1,int no2)
        {
            return no1*no2;
        }
}
```

### Types Of Inheritance

* Single Level Inheritance
* Multi Level Inheritance
* Multiple Inheritance
* Hierarchical Inheritance
* Hybrid Inheritance

### <b>Single Level inheritance</b>

One child class inherits one parent class

![image](https://media.geeksforgeeks.org/wp-content/uploads/single-inheritance.png)

### <b>Multi Level Inheritance</b>

As the name suggests, in this type of inheritance, there are multiple levels of inheritance.  This is analogous to grand parents, then parents then children.

![image](https://user-images.githubusercontent.com/26179770/37459322-b018b41c-286d-11e8-9382-dc31f5690ccd.png)

### <b>Multiple Inheritance</b>

When one child cass inherits properties of  more than one classes.

![image](https://media.geeksforgeeks.org/wp-content/uploads/multiple-inheritance.png)

### <b>Hierarchical Inheritance</b>

In this case the inheritance pattern forms a hierarchy, i.e., there are multiple derived classes of same base class.

![image](https://user-images.githubusercontent.com/26179770/37459413-f5d3db94-286d-11e8-9e82-c2675b36c8ac.png)

### <b>Hybrid Inheritance</b>

Hybrid Inheritance is implemented by combining more than one type of inheritance. For example: Combining Hierarchical inheritance and Multiple Inheritance.

![imageFor markdown syntax](https://media.geeksforgeeks.org/wp-content/uploads/Hybrid-Inheritance.png)

You can refere following URL for more information on Inheritance
[**click here**](https://www.geeksforgeeks.org/inheritance-in-c/)



<br />


## Resouces :-
1. Object-Oriented Programming with C++ by E. Balgurusamy
2. https://www.geeksforgeeks.org/object-oriented-programming-in-cpp/?ref=lbp

3. https://www.indeed.com/career-advice/career-development/what-is-object-oriented-programming
   
4.  https://commonmark.org/help/  (For markdown syntax)