# Advanced Java OOP Assignment
## Part 2 – Theory Questions and Answers

**Subject:** Object-Oriented Programming using JAVA

### Q1. What are the four main principles of Object-Oriented Programming (OOP)?

The four main principles of OOP are:

1. **Encapsulation:** Wrapping data and methods into a single unit called a class.
2. **Inheritance:** Allowing one class to acquire the properties and methods of another class.
3. **Polymorphism:** Allowing one method or object to perform different tasks.
4. **Abstraction:** Hiding implementation details and showing only essential features.

These principles make Java programs reusable, secure, flexible and easier to maintain.

### Q2. What is the difference between a class and an object in Java?

- **Class:** A class is a blueprint or template used to create objects.
- **Object:** An object is an instance of a class that contains data and methods.

Example:
```java
class Student {
    String name = "Rahul";

    void display() {
        System.out.println(name);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();
        s1.display();
    }
}
```
Here, `Student` is the class and `s1` is its object.

### Q3. What is a constructor in Java? Explain its types.

A constructor is a special method-like block used to initialize objects. It has the same name as the class and does not have a return type.

Types of constructors:

1. **Default constructor:** Provided automatically by Java when no constructor is defined.
2. **No-argument constructor:** A constructor explicitly written without parameters.
3. **Parameterized constructor:** A constructor that accepts arguments to initialize object data.

Example:
```java
class Student {
    String name;

    Student(String n) {
        name = n;
    }

    public static void main(String[] args) {
        Student s = new Student("Rahul");
        System.out.println(s.name);
    }
}
```

### Q4. Differentiate between method overloading and method overriding.

**Method Overloading:**
- Same method name with different parameters.
- Usually occurs within the same class.
- Represents compile-time polymorphism.

**Method Overriding:**
- A child class provides its own implementation of a parent class method.
- Requires inheritance.
- Represents runtime polymorphism.

Example:
```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```
Both methods have the same name but different parameters, so this is overloading.

### Q5. What is the difference between an abstract class and an interface?

**Abstract Class:**
- Declared using the `abstract` keyword.
- Can contain abstract and concrete methods.
- Can have constructors and instance variables.
- A class can extend only one class.

**Interface:**
- Declared using the `interface` keyword.
- Defines a contract that implementing classes must follow.
- Can contain abstract, default and static methods.
- A class can implement multiple interfaces.

Both are used to achieve abstraction in Java.

### Q6. What are access modifiers in Java? Explain their types.

Access modifiers control the visibility and accessibility of classes, methods and variables.

There are four main access levels:

1. **Public:** Accessible from anywhere.
2. **Private:** Accessible only within the same class.
3. **Protected:** Accessible within the same package and by subclasses, subject to Java access rules.
4. **Default:** Accessible only within the same package.

Access modifiers help protect data and provide controlled access to program components.

### Q7. What is exception handling in Java? Explain try, catch, finally, throw and throws.

Exception handling is a mechanism used to handle runtime errors so that the normal execution of a program can continue when possible.

Important keywords:

1. `try`: Contains code that might generate an exception.
2. `catch`: Handles the exception.
3. `finally`: Executes after try/catch, whether an exception occurs or not, except in unusual termination cases.
4. `throw`: Used to explicitly throw an exception.
5. `throws`: Declares exceptions that a method may pass to its caller.

Example:
```java
public class Main {
    public static void main(String[] args) {
        try {
            int a = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero");
        } finally {
            System.out.println("Program completed");
        }
    }
}
```

### Q8. What is file handling in Java? Explain FileReader, FileWriter, BufferedReader and BufferedWriter.

File handling allows Java programs to create, read and write data in files.

Important classes:

1. **File:** Used to represent file and directory paths and perform file-related operations.
2. **FileReader:** Reads character data from a file.
3. **FileWriter:** Writes character data into a file.
4. **BufferedReader:** Reads text efficiently using a buffer.
5. **BufferedWriter:** Writes text efficiently using a buffer.

File handling is useful for storing information permanently, even after the program stops running.

### Q9. What is multithreading in Java? Explain its advantages.

Multithreading is the process of executing multiple threads within a single program.

A thread is a lightweight unit of execution.

Threads can be created using:

1. Extending the `Thread` class.
2. Implementing the `Runnable` interface.

Advantages:

- Improves CPU utilization.
- Allows multiple tasks to run concurrently.
- Makes applications more responsive.
- Helps perform background operations.

Example:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t = new MyThread();
        t.start();
    }
}
```

### Q10. What is the Java Collections Framework? Explain List, Set and Map.

The Java Collections Framework is a group of classes and interfaces used to store and manage collections of objects.

Its main interfaces include:

1. **List:** Stores elements in an ordered collection and allows duplicates. Example: `ArrayList`.
2. **Set:** Stores unique elements and does not allow duplicates. Example: `HashSet`.
3. **Map:** Stores data in key-value pairs. Keys must be unique. Example: `HashMap`.

Advantages:

1. Makes data storage and management easier.
2. Provides built-in methods for searching and sorting.
3. Reduces programming effort.
4. Supports dynamic data structures.


