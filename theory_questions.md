# Day12_JavaIgnite
Differentiate between:

Method Overloading

Method Overriding

Provide one example scenario for each.

Ans-
method overloading 
same method name with different parameters   	        Same method name and same parameters
Happens in same class	                              Happens between parent and child class
Used to perform similar tasks in different ways     	Used to change parent class behavior




Example of Method Overloading
class Calculator {

    void add(int a, int b) {

        System.out.println(a + b);
    }

    void add(int a, int b, int c) {

        System.out.println(a + b + c);
    }
}

Example of Method Overriding
class Animal {

    void sound() {

        System.out.println("Animal Sound");
    }
}

class Dog extends Animal {

    @Override
    void sound() {

        System.out.println("Bark");
    }
}





Question 2

What is the purpose of Wrapper Classes?


Ans->
Wrapper classes convert primitive data types into objects.

Why can't we directly use primitive data types in some Java collections?

Ans->Some Java collections like

ArrayList
HashMap
LinkedList

store only objects, not primitive types.




Question 3

Differentiate between:

FileWriter

FileOutputStream


Ans-> the difference between the filewriter and the file ouutputstreammer is written below 
FileWriter	                          FileOutputStream
Used for writing text data          	Used for writing binary data
Writes characters	                    Writes bytes
Best for .txt files                 	Best for images, audio, PDF, etc.

When would you choose one over the other?

Ans->Use FileWriter for text files.
Use FileOutputStream for binary files or byte-level operations.



Explain Inheritance using a real-world example.


Ans->this is the real wrold example of the inheritance 

class Vehicle {

    void start() {

        System.out.println("Vehicle Starts");
    }
}

class Car extends Vehicle {

    void musicSystem() {

        System.out.println("Music System On");
    }
}

How does inheritance help reduce code duplication?


    Ans->>Without inheritance:

Every class must write common code again.

With inheritance:

Common code is written once in parent class and reused by child classes.

Example:

If all vehicles have:

start()
stop()
fuel()

these methods are written once in Vehicle class.

All child classes reuse them.

    


Important Interview Question - 

class Animal {
    void sound() {
        System.out.println("Animal Sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Bark");
    }
}

Animal a = new Dog();
a.sound();

What will be the output?

Explain why.

Ans->>>
Bark
Explanation
a is reference of parent class Animal.
Object created is of child class Dog.

Java checks the object type at runtime.

Since object is Dog, overridden method in Dog class is called.

This is called:

Runtime Polymorphism
Dynamic Method Dispatch


