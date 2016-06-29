---
title: Subclassing and Interfaces
type: Homework
duration: "1:00"
creator:
    name: Charlie Drews
    city: NYC
---

# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Subclassing, Abstract Classes, and Interfaces

> ***Note:*** _You can discuss with classmates, but everyone must submit their own answers_

## Exercise

#### Requirements

- Fork this repo, then add your answers direcly to this **readme.md** file
  - After forking, you can clone, edit the readme in the text editor of your choice, and push back to Github...
  - Or, you can edit the readme [right from the browser](https://help.github.com/articles/editing-files-in-your-repository/)
- After adding your answers, submit a **pull request**

#### Questions

1. What is the difference between *member variables* (also called *instance variables*) and *class variables* (w/ keyword `static`)? Which can be accessed without creating an instance of the class?
- Member variables are created and accessed within the scope of that class instance.
- Class variables with keyword static remain throughout the entirety of the program.

2. Does it make sense to write  *getter* and *setter* methods for a `public` member variable? What about `private` variables?
- You can. Writing getter and setter methods for 'public' member variables allows for those instance variables to be accessed outside of the scope of the class they were created in. Only if a new instance of the object is created can the public instance methods be acessed outside of the class. 
-'Private' member variables are not able to be accessed outside of the class they are created in so the getter and setter method would have the value passed into the class's method modify the member variable.

3. What are some benefits of making member variables `private`?
- Making member variables private allows the current class to access the member vaiable, but not another class or subclass. 

4. If class A extends class B, which is the super class and which is the sub class? Which would you call parent, and which would you call child?
- ClassB is the super class or parent class. ClassA is the sub class and the child of ClassB.

5. What does it mean for a class to *inherit* methods and/or variables from its parent class?
- When a class inherits methods and variables from its parent class the child class has the ability to access the information contained within the variables and perform the methods of its parent including the ability to override those methods and perform its own unique functionality.

6. Consider the following code, where class Refrigerator extends class Appliance, and `getTemperature()` is a method in Refrigertor, but NOT in Appliance:
  ```
  Appliance myAppliance = new Refrigerator();
  double temperature = myAppliance.getTemperature();
  ```
  Why will this call to `getTemperature()` cause an error? How will *casting* help solve this issue?
- Yes. The mothod will not be recognized. In order for the method to be recognize myAppliance should be casted to a Refrigerator object or to the Refrigerator class. Essentially when myAppliance is casted to type Refrigerator myAppliance will be recognized as a Refrigerator and not as an Appliance. Refrigerator is a type of Appliance.

7. In a normal class (also called a *concrete* class), do you need to *implement* all of the methods, or can your simply *declare* some? What about in an `abstract` class?
- When an abstract method is declared in an abstract class the sub classes of that abstract class must implement the abtract class even if the method body is empty when implemented. In a concrete class all of the methods must be implemented even if they are empty when implemented.

8. What about an `interface`? Can you implement any methods in an interface? Can you declare methods in an interface?
- In an Interface the methods are not implemented, they are declared. All methods defined in an interface class are abstract by default.

9. Can you create an instance of an `abstract` class? Also, look up the Java keyword `final` and see if you can explain why a class CANNOT be both `abstract` and `final`.
- Yes, an instance of an abstract class can be created. The Java documentation says "You can declare some or all of a class's methods final. You use the final keyword in a method declaration to indicate that the method cannot be overridden by subclasses. The Object class does this—a number of its methods are final." (Meaning that all number objects created cannot be changed.) abstract and final cannt be declared together because declaring something abstract is the idea of having a declared abstract method implemented by its sub class. Declaring the abstract methods / classes final would not allow each of the overriden methods to function. Making something that's meant to be changed unable to be changed defeats the purpose of using something that can be changed to begin with.

10. What happens when a method *overrides* another method? If a parent and child class have methods with the same name, when you call that method on an instance of the child class, which implementation of the method will be executed?
- The Java documentation says "The ability of a subclass to override a method allows a class to inherit from a superclass whose behavior is "close enough" and then to modify behavior as needed. The overriding method has the same name, number and type of parameters, and return type as the method that it overrides. An overriding method can also return a subtype of the type returned by the overridden method. This subtype is called a covariant return type."

If a parent and child class have methods with the same name, when you call that method on an instance of the child class the child class's version of the method would be used.

11. What is the relationship between `List`, `LinkedList`, and `ArrayList`? Why do we call a method *polymorphic* if it takes an input of type `List` rather than an input of type `LinkedList` or `Arraylist`, and why is that useful?
- The relationship between List, LinkedList, and ArrayList is that they are all kinds of Collections. The List is a special kind of a Collection and LinkedList & ArrayList are a special kind of List.

The documentation defines List as "an ordered collection (sometimes called a sequence). Lists can contain duplicate elements. The user of a List generally has precise control over where in the list each element is inserted and can access elements by their integer index (position)."

The documentation defines ArrayList as a "Resizable-array implementation of the List interface."

The documentation defines LinkedList as a "Doubly-linked list implementation of the List and Deque interfaces."

The documentation defines Polymophism with "The dictionary definition of polymorphism refers to a principle in biology in which an organism or species can have many different forms or stages. This principle can also be applied to object-oriented programming and languages like the Java language. Subclasses of a class can define their own unique behaviors and yet share some of the same functionality of the parent class."

So...

	List<String> myList = new ArrayList<>();

...is an ArrayList named myList. This ArrayList named myList has many of the same properties as ArrayList's parent class List.

#### Deliverable

This file, with your answers added

## Additional Resources

Refer to the [Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/classes-lesson), the [Subclassing lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/subclasses-lesson), and the [Interfaces & Abstract Classes lesson](https://github.com/ga-adi-nyc/Course-Materials/tree/master/lessons/java-essentials/interfaces-and-abstract-classes-lesson).

Feel free to google these concepts as well. There are plenty of Java tutorial websites and StackOverflow posts that can help you. But be sure to write up your answers in your own words - copying and pasting some text does NOT help you actually learn!
