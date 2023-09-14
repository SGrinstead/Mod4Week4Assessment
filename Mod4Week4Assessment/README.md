# Week 4 Assessment

### Setup
* Fork and clone this repository
* Open your forked repo in Visual Studio.
* Complete the two exercises and the questions

## Exercise 1: Inheritance and Dependency Injection (8 points)

Open up `Program.cs` and run your program. It should run with no errors, if you get an error reach out to your instructor.

This exercise involves some refactoring and some new features.

**Step 1:** Currently there are two classess `Student` and `Teacher` that have a lot of repeated code between them. Create a new class `Person` that will be the base class. Then update `Student` and `Teacher` to be derived from `Person`. Include as much in your `Person` class as you can to keep your code DRY (Don't Repeat Yourself). 

**Testing Step 1:** Uncomment the code under "Step 1:" in the Main method. That code should now run without error.

**Step 2:** Implement a new class called `School` that uses dependency injection and takes in a list of people as a dependency. Implement a method called `ListBirthdays` in your school class that calls the `GetBirthday` method and prints to the console each student and teacher's birthday.

**Testing Step 2:** Uncomment the code under "Step 2:" in the Main method. That code should now run without error and output a bunch of names and birthdays.

Ungraded extra challenge: If you have time, improve the way the birthdays are output. Can you group them by month or by Student/Teacher?

### Exercise 2: Interfaces (4 points)
Open up `InterfacePractice.cs`. You should not need to run this file, you will just edit it.

**Step 1:** Take a look at the two classes `Car` and `Bicycle`. They both implement an interface called `InterfaceNameHere`. Replace all three uses of `InterfaceNameHere` with a fitting name for this interface.

**Step 2:** The interface has already been created for you on line 5. Fill in the details for any methods and/or properties that make sense based on the two classes implementing this interface.

## Questions (8 points)

Edit this file with your answers.

1. What are some of the benefits of using inheritance? (1 point)
    * By using inheritance, you can use the methods and properties from a parent class in every child class, so you don't have
	to repeat those methods and properties in each child class.
2. What might be some of the disadvantages of using inheritance? (1 point)
    * Inheritance can complicate your code and make testing and bugfixing harder because of the abstraction of the parent class.
	If there is a parent class for your parent class, this can get even more complicated.

3. How would you describe the difference between the base class and the derived class when working with inheritance? (1 point)
	* The base or parent class is a more general class, while the derived or child class is more specific. In the case of the
	person and teacher classes from this test, the person class has general properties and methods like Name, Birthday, and
	GetBirthday that the teacher inherits, while the teacher has specific properties and methods like the 
	subject they teach and a specific greeting.

4.  What happens if you define the same method in the parent class and the child class? (1 point)
	* Because the child class has more specific information, the child class' version of the method will take priority.

5. In your own words, how would you define an Interface? (1 point)
    * An interface is an outline of a class for any class that implements it. It lays out all the methods and properties that
	must be defined.

6. Does a class implementing an interface need to implement all of the methods in that interface? Why or why not? (1 point)
    * Yes, The class must implement every method and property in the interface, or you will get an error.

7. Both Inheritance and Interfaces use the `:` symbol after a class name. If you're looking at a class, what's one thing that can help you determine if the class is implementing an interface of extending a base class? (1 point)
	* Most interfaces have a capital I at the start of their name, but if you want to be sure, you can also hover over it in
	Visual Studio and it will either say it is an Interface or a class. They are also slightly different colors (at least in dark mode)

8. If asked in an interview, how would you describe the purpose of the IOC container in a .NET application? (1 point)
	* An IOC container is responsible for automatically setting up and injecting dependencies in your program when you start it.
	This is important for lots of behind-the-scenes work that .NET does, like setting up the connection to the database when
	the program starts.


## Rubric

This assessment has a total of 20 points.  A score of 15 or higher is a pass.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
