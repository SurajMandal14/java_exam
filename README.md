# Java Final Exam Preparation Guide

## Introduction
This guide provides a structured overview of key topics and question patterns for the Java final exam, based on the syllabus provided. It aims to cover important concepts with explanations and relevant Java code examples to aid in your preparation.

## Exam Pattern

### Section A: Theory Questions
-   **Number of Questions:** 4
-   **Marks per Question:** 5
-   **Total Marks:** 4 × 5 = 20 Marks
-   **Instructions:** Support your answers with relevant programming examples wherever applicable.

### Section B: Programming Questions
-   **Number of Questions:** Answer any 3 out of 5
-   **Marks per Question:** 10
-   **Total Marks:** 3 × 10 = 30 Marks
-   **Instructions:** Write complete program (including main method) clearly and ensure they are free from logical and syntactical errors.

**Total Marks: 50**

---

## Important Questions & Answers

### Unit 1: Java Basics

#### 1. Features of Java
Java is a popular, versatile, and powerful programming language known for several key features:

*   **Simple:** Java was designed to be easy to learn, with syntax similar to C++ but omitting complex features like pointers and multiple inheritance (in terms of classes).
*   **Object-Oriented:** Java is purely object-oriented. Everything in Java is an object (except for primitive data types). It supports core OOP concepts like Encapsulation, Inheritance, Polymorphism, and Abstraction.
*   **Platform Independent (Write Once, Run Anywhere - WORA):** Java code is compiled into an intermediate form called bytecode (`.class` files). This bytecode can run on any platform that has a Java Virtual Machine (JVM) without needing to be recompiled.
*   **Robust:** Java emphasizes early checking for possible errors, both at compile-time and run-time. It has strong memory management (automatic garbage collection) and exception handling mechanisms.
*   **Secure:** Java's security features include a security manager that defines access to system resources, bytecode verification, and the absence of explicit pointers, which prevents unauthorized memory access.
*   **High Performance:** While Java is an interpreted language (bytecode is interpreted by JVM), modern JVMs use Just-In-Time (JIT) compilers to convert bytecode into native machine code at runtime, significantly improving performance.
*   **Multithreaded:** Java has built-in support for multithreading, allowing concurrent execution of different parts of a program. This improves performance and responsiveness, especially for applications with GUIs or network operations.
*   **Distributed:** Java is designed for distributed environments. It has libraries for network programming (e.g., `java.net` package) and supports protocols like TCP/IP and UDP. RMI (Remote Method Invocation) and EJB (Enterprise JavaBeans) enable building distributed applications.
*   **Dynamic:** Java can adapt to an evolving environment. Java programs can carry extensive amounts of run-time type information that can be used to verify and resolve accesses to objects at run-time.

#### 2. Data types
Java has two main categories of data types:

*   **Primitive Data Types:** These are the most basic data types available in Java. They are predefined by the language and named by a reserved keyword.
    *   **byte:** 8-bit signed two's complement integer. Range: -128 to 127. Default: 0.
        ```java
        byte b = 100;
        ```
    *   **short:** 16-bit signed two's complement integer. Range: -32,768 to 32,767. Default: 0.
        ```java
        short s = 10000;
        ```
    *   **int:** 32-bit signed two's complement integer. Range: -2<sup>31</sup> to 2<sup>31</sup>-1. Default: 0. This is the most commonly used integer type.
        ```java
        int i = 100000;
        ```
    *   **long:** 64-bit signed two's complement integer. Range: -2<sup>63</sup> to 2<sup>63</sup>-1. Used when a wider range than `int` is needed. Suffix `L` or `l`. Default: 0L.
        ```java
        long l = 100000L;
        ```
    *   **float:** Single-precision 32-bit IEEE 754 floating point. Suffix `F` or `f`. Default: 0.0f.
        ```java
        float f = 234.5f;
        ```
    *   **double:** Double-precision 64-bit IEEE 754 floating point. This is the default type for decimal numbers. Suffix `D` or `d` (optional). Default: 0.0d.
        ```java
        double d = 123.4;
        ```
    *   **boolean:** Represents one bit of information. Can have only two possible values: `true` or `false`. Default: `false`.
        ```java
        boolean isValid = true;
        ```
    *   **char:** Single 16-bit Unicode character. Range: `\u0000` (or 0) to `\uffff` (or 65,535 inclusive). Can represent characters from virtually all scripts.
        ```java
        char letter = 'A';
        char unicodeChar = '\u0058'; // Represents 'X'
        ```

*   **Reference/Object Data Types:** These are created using defined constructors of the classes. They are used to access objects.
    *   Examples: `String`, `Array`, `Class`, `Interface`.
    *   Reference variables store the memory address of an object.
    *   Default value for any reference variable is `null`.
    ```java
    String greeting = "Hello, World!"; // String is a class
    int[] numbers = new int[5];       // Array
    Object obj = new Object();        // Generic Object
    ```

#### 3. Control statements
Control statements in Java are used to control the flow of execution in a program.

*   **Selection Statements (Decision Making):**
    *   **`if` statement:** Executes a block of code if a condition is true.
        ```java
        public class IfExample {
            public static void main(String[] args) {
                int number = 10;
                if (number > 5) {
                    System.out.println("Number is greater than 5."); // Output
                }
            }
        }
        ```
    *   **`if-else` statement:** Executes one block of code if a condition is true, and another block if it's false.
        ```java
        public class IfElseExample {
            public static void main(String[] args) {
                int number = 3;
                if (number > 5) {
                    System.out.println("Number is greater than 5.");
                } else {
                    System.out.println("Number is not greater than 5."); // Output
                }
            }
        }
        ```
    *   **`if-else-if` ladder:** Used to test multiple conditions.
        ```java
        public class IfElseIfExample {
            public static void main(String[] args) {
                int marks = 75;
                if (marks >= 90) {
                    System.out.println("Grade A");
                } else if (marks >= 80) {
                    System.out.println("Grade B");
                } else if (marks >= 70) {
                    System.out.println("Grade C"); // Output
                } else {
                    System.out.println("Grade D");
                }
            }
        }
        ```
    *   **`switch` statement:** Selects one of many code blocks to be executed.
        ```java
        public class SwitchExample {
            public static void main(String[] args) {
                int day = 3;
                String dayString;
                switch (day) {
                    case 1: dayString = "Monday"; break;
                    case 2: dayString = "Tuesday"; break;
                    case 3: dayString = "Wednesday"; break; // Matched
                    case 4: dayString = "Thursday"; break;
                    case 5: dayString = "Friday"; break;
                    default: dayString = "Weekend"; break;
                }
                System.out.println(dayString); // Output: Wednesday
            }
        }
        ```

*   **Iteration Statements (Loops):**
    *   **`for` loop:** Executes a block of code a specific number of times.
        ```java
        public class ForLoopExample {
            public static void main(String[] args) {
                for (int i = 0; i < 5; i++) {
                    System.out.println("Iteration: " + i);
                }
            }
        }
        ```
    *   **`while` loop:** Executes a block of code as long as a condition is true.
        ```java
        public class WhileLoopExample {
            public static void main(String[] args) {
                int i = 0;
                while (i < 5) {
                    System.out.println("Iteration: " + i);
                    i++;
                }
            }
        }
        ```
    *   **`do-while` loop:** Executes a block of code once, and then repeats the loop as long as a condition is true. The condition is checked *after* the loop body.
        ```java
        public class DoWhileLoopExample {
            public static void main(String[] args) {
                int i = 0;
                do {
                    System.out.println("Iteration: " + i);
                    i++;
                } while (i < 5);
            }
        }
        ```
    *   **Enhanced `for` loop (for-each loop):** Used to iterate through elements of arrays and collections.
        ```java
        public class EnhancedForLoopExample {
            public static void main(String[] args) {
                int[] numbers = {1, 2, 3, 4, 5};
                for (int number : numbers) {
                    System.out.println("Number: " + number);
                }

                String[] names = {"Alice", "Bob", "Charlie"};
                for (String name : names) {
                    System.out.println("Name: " + name);
                }
            }
        }
        ```

*   **Jump Statements:**
    *   **`break`:** Terminates the loop or switch statement.
        ```java
        public class BreakExample {
            public static void main(String[] args) {
                for (int i = 0; i < 10; i++) {
                    if (i == 5) {
                        break; // Exits the loop when i is 5
                    }
                    System.out.println("i: " + i);
                }
            }
        }
        ```
    *   **`continue`:** Skips the current iteration of a loop and proceeds to the next iteration.
        ```java
        public class ContinueExample {
            public static void main(String[] args) {
                for (int i = 0; i < 10; i++) {
                    if (i % 2 == 0) {
                        continue; // Skips even numbers
                    }
                    System.out.println("Odd number: " + i);
                }
            }
        }
        ```
    *   **`return`:** Used to exit from a method, with or without a value.
        ```java
        public class ReturnExample {
            public static int add(int a, int b) {
                return a + b; // Returns the sum
            }
            public static void printMessage() {
                System.out.println("Hello!");
                return; // Optional for void methods, exits the method
                // System.out.println("This won't be printed.");
            }
            public static void main(String[] args) {
                int sum = add(5, 3);
                System.out.println("Sum: " + sum);
                printMessage();
            }
        }
        ```

#### 4. Keywords and use cases
Java keywords are reserved words that have predefined meanings in the language. They cannot be used as identifiers (names for variables, methods, classes, etc.).

Here are some important keywords and their use cases:

*   **`abstract`**:
    *   Used to declare an abstract class (a class that cannot be instantiated and may contain abstract methods).
    *   Used to declare an abstract method (a method without a body, to be implemented by subclasses).
    ```java
    abstract class Shape { // abstract class
        abstract void draw(); // abstract method
    }
    class Circle extends Shape {
        void draw() { System.out.println("Drawing Circle"); }
    }
    ```
*   **`class`**: Used to declare a class.
    ```java
    class MyClass { /* ... */ }
    ```
*   **`interface`**: Used to declare an interface (a collection of abstract methods and constants).
    ```java
    interface Drawable { void draw(); }
    ```
*   **`extends`**: Used in class declarations to specify the superclass (for inheritance).
    ```java
    class Animal { /* ... */ }
    class Dog extends Animal { /* ... */ } // Dog inherits from Animal
    ```
*   **`implements`**: Used in class declarations to specify one or more interfaces that the class will implement.
    ```java
    class MyCanvas implements Drawable {
        public void draw() { System.out.println("Drawing on canvas"); }
    }
    ```
*   **`public`, `private`, `protected`**: Access modifiers that control the visibility of classes, methods, and variables.
    *   `public`: Accessible from any other class.
    *   `private`: Accessible only within the declared class.
    *   `protected`: Accessible within the same package and by subclasses in other packages.
*   **`static`**:
    *   Used to create class variables (shared among all instances of a class).
    *   Used to create class methods (can be called without creating an instance of the class).
    *   Used for static blocks (executed when the class is loaded).
    ```java
    class Counter {
        static int count = 0; // static variable
        Counter() { count++; }
        static void showCount() { // static method
            System.out.println("Count: " + count);
        }
    }
    ```
*   **`final`**:
    *   Used to declare a constant variable (its value cannot be changed).
    *   Used to prevent method overriding in a subclass.
    *   Used to prevent a class from being subclassed (inherited).
    ```java
    final class ImmutableClass { /* ... */ }
    class Parent {
        final void display() { System.out.println("Final method"); }
    }
    // class Child extends Parent {
    //     void display() {} // Error: cannot override final method
    // }
    final int MAX_VALUE = 100;
    ```
*   **`this`**: Refers to the current instance of the class. Used to:
    *   Distinguish instance variables from local variables if they have the same name.
    *   Call another constructor of the same class (constructor chaining).
    *   Pass the current object as an argument to a method.
    ```java
    class Box {
        int width;
        Box(int width) { this.width = width; } // Disambiguate
        Box() { this(10); } // Call another constructor
    }
    ```
*   **`super`**: Refers to the immediate parent class object. Used to:
    *   Access members (fields or methods) of the superclass that have been hidden by the subclass.
    *   Call the superclass constructor from the subclass constructor.
    ```java
    class Vehicle {
        String type = "Generic Vehicle";
        Vehicle() { System.out.println("Vehicle constructor"); }
        void displayType() { System.out.println(type); }
    }
    class Car extends Vehicle {
        String type = "Automobile";
        Car() {
            super(); // Calls Vehicle constructor
            System.out.println("Car constructor");
        }
        void displayType() {
            super.displayType(); // Calls Vehicle's displayType
            System.out.println(this.type); // Accesses Car's type
            System.out.println(super.type); // Accesses Vehicle's type
        }
    }
    ```
*   **`new`**: Used to create new objects (instances of classes).
    ```java
    MyClass obj = new MyClass();
    ```
*   **`instanceof`**: Operator used to test whether an object is an instance of a particular class or interface.
    ```java
    Animal myAnimal = new Dog();
    if (myAnimal instanceof Dog) {
        System.out.println("It's a Dog!");
    }
    ```
*   **`void`**: Indicates that a method does not return any value.
    ```java
    void printMessage() { System.out.println("Hello"); }
    ```
*   **`return`**: Used to exit from a method, optionally returning a value.
*   **`try`, `catch`, `finally`, `throw`, `throws`**: Used for exception handling (covered in Unit 2).
*   **`synchronized`**: Used in multithreading to control access to shared resources (covered in Unit 3).
*   **`package`**: Used to declare a Java package.
    ```java
    package com.example.myapp;
    ```
*   **`import`**: Used to import classes or entire packages into the current Java file.
    ```java
    import java.util.ArrayList;
    import java.io.*; // Imports all classes from java.io
    ```

#### 5. Interfaces, inheritance, abstract classes

*   **Inheritance:**
    *   A mechanism where a new class (subclass or derived class) acquires the properties (fields) and behaviors (methods) of an existing class (superclass or base class).
    *   Promotes code reusability and establishes an "is-a" relationship (e.g., a `Dog` is an `Animal`).
    *   Java supports single inheritance for classes (a class can extend only one superclass) but multiple inheritance through interfaces.
    *   Uses the `extends` keyword.

    ```java
    // Superclass
    class Animal {
        String name;
        public Animal(String name) {
            this.name = name;
        }
        public void eat() {
            System.out.println(name + " is eating.");
        }
        public void makeSound() {
            System.out.println(name + " makes a sound.");
        }
    }

    // Subclass
    class Dog extends Animal {
        public Dog(String name) {
            super(name); // Call superclass constructor
        }
        // Overriding the makeSound method
        @Override
        public void makeSound() {
            System.out.println(name + " barks.");
        }
        public void fetch() {
            System.out.println(name + " is fetching.");
        }
    }

    public class InheritanceExample {
        public static void main(String[] args) {
            Animal myAnimal = new Animal("Generic Animal");
            myAnimal.eat();
            myAnimal.makeSound();

            Dog myDog = new Dog("Buddy");
            myDog.eat();       // Inherited from Animal
            myDog.makeSound(); // Overridden in Dog
            myDog.fetch();     // Specific to Dog
        }
    }
    ```

*   **Abstract Classes:**
    *   A class that is declared with the `abstract` keyword.
    *   Cannot be instantiated (you cannot create objects of an abstract class).
    *   Can have abstract methods (methods without a body) and concrete methods (methods with implementation).
    *   If a class contains one or more abstract methods, it must be declared abstract.
    *   Subclasses of an abstract class must either implement all abstract methods of the superclass or be declared abstract themselves.
    *   Used to provide a common base for subclasses, defining a contract that subclasses must follow.

    ```java
    // Abstract class
    abstract class Shape {
        String color;

        public Shape(String color) {
            this.color = color;
        }

        // Abstract method (no implementation)
        public abstract double getArea();

        // Concrete method
        public String getColor() {
            return color;
        }
    }

    class CircleShape extends Shape {
        double radius;
        public CircleShape(String color, double radius) {
            super(color);
            this.radius = radius;
        }
        // Implementation of abstract method
        @Override
        public double getArea() {
            return Math.PI * radius * radius;
        }
    }

    class RectangleShape extends Shape {
        double width, height;
        public RectangleShape(String color, double width, double height) {
            super(color);
            this.width = width;
            this.height = height;
        }
        // Implementation of abstract method
        @Override
        public double getArea() {
            return width * height;
        }
    }

    public class AbstractClassExample {
        public static void main(String[] args) {
            // Shape myShape = new Shape("Red"); // Error: Cannot instantiate abstract class

            Shape circle = new CircleShape("Red", 5.0);
            System.out.println("Circle color: " + circle.getColor());
            System.out.println("Circle area: " + circle.getArea());

            Shape rectangle = new RectangleShape("Blue", 4.0, 6.0);
            System.out.println("Rectangle color: " + rectangle.getColor());
            System.out.println("Rectangle area: " + rectangle.getArea());
        }
    }
    ```

*   **Interfaces:**
    *   A completely abstract type that is used to group related methods with empty bodies.
    *   Declared using the `interface` keyword.
    *   Can contain only abstract methods (by default `public abstract`), static methods (Java 8+), default methods (Java 8+), and constant declarations (by default `public static final`).
    *   A class can `implement` one or more interfaces (achieving multiple inheritance of type).
    *   Interfaces define a contract for what a class can do, without specifying how it does it.

    ```java
    // Interface
    interface Drawable {
        void draw(); // public abstract by default
        // Java 8 default method
        default void getDimensions() {
            System.out.println("Default dimensions calculation.");
        }
        // Java 8 static method
        static int getSides() {
            return 0; // Generic, to be overridden or used as is
        }
    }

    interface Movable {
        void move(int x, int y);
    }

    class GraphicCircle implements Drawable, Movable { // Implementing multiple interfaces
        int x, y, radius;
        public GraphicCircle(int x, int y, int radius) {
            this.x = x;
            this.y = y;
            this.radius = radius;
        }

        @Override
        public void draw() {
            System.out.println("Drawing Circle at (" + x + "," + y + ") with radius " + radius);
        }

        @Override
        public void move(int newX, int newY) {
            this.x = newX;
            this.y = newY;
            System.out.println("Moved Circle to (" + x + "," + y + ")");
        }

        // Optionally override default method
        @Override
        public void getDimensions() {
            System.out.println("Circle dimensions: radius = " + radius);
        }
    }

    public class InterfaceExample {
        public static void main(String[] args) {
            GraphicCircle gc = new GraphicCircle(10, 20, 5);
            gc.draw();
            gc.move(15, 25);
            gc.getDimensions();

            System.out.println("Sides (from interface static method): " + Drawable.getSides());

            Drawable d = new GraphicCircle(1,2,3); // Can use interface as type
            d.draw();
        }
    }
    ```

---
### Unit 2: Exception Handling & Polymorphism

#### 1. Exception handling keywords: `try`, `catch`, `finally`, `throw`, `throws`

Exceptions are runtime errors or unexpected conditions that a program may encounter during its execution. Java provides a robust mechanism to handle these exceptions.

*   **`try`**: The `try` block encloses the code that might throw an exception. It must be followed by either a `catch` block or a `finally` block (or both).
*   **`catch`**: The `catch` block is used to handle the exception. It catches an exception of a specific type thrown from the `try` block. You can have multiple `catch` blocks to handle different types of exceptions.
*   **`finally`**: The `finally` block is always executed, regardless of whether an exception is thrown or caught. It's typically used for cleanup code, like closing files or releasing resources.
*   **`throw`**: The `throw` keyword is used to explicitly throw an exception (either a built-in exception or a user-defined one).
*   **`throws`**: The `throws` keyword is used in a method signature to declare that the method might throw one or more specified exceptions. It indicates to the caller that they need to handle these potential exceptions.

**Example:**

```java
public class ExceptionHandlingDemo {

    // Method that might throw an ArithmeticException
    public static int divide(int a, int b) {
        if (b == 0) {
            // Explicitly throwing an exception
            throw new ArithmeticException("Division by zero is not allowed.");
        }
        return a / b;
    }

    // Method declaring it might throw an IOException (checked exception)
    public static void readFile(String fileName) throws java.io.IOException {
        // Simulating file reading that might throw IOException
        if (fileName == null || fileName.isEmpty()) {
            throw new java.io.IOException("File name cannot be null or empty.");
        }
        System.out.println("Attempting to read file: " + fileName);
        // Actual file reading logic would go here
    }

    public static void main(String[] args) {
        // Example 1: try-catch-finally
        try {
            int result = 100 / 0; // This will cause an ArithmeticException
            System.out.println("Result: " + result); // This line won't be executed
        } catch (ArithmeticException e) {
            System.err.println("Caught ArithmeticException: " + e.getMessage());
        } finally {
            System.out.println("Finally block for division executed.");
        }

        System.out.println("------------------------------------");

        // Example 2: try-catch for method that throws an exception
        try {
            int result = divide(10, 0);
            System.out.println("Division result: " + result);
        } catch (ArithmeticException e) {
            System.err.println("Caught exception from divide method: " + e.getMessage());
        }

        System.out.println("------------------------------------");

        // Example 3: Handling checked exception declared with 'throws'
        try {
            readFile("myFile.txt");
            readFile(null); // This will throw IOException
        } catch (java.io.IOException e) {
            System.err.println("Caught IOException: " + e.getMessage());
        } finally {
            System.out.println("Finally block for file reading executed.");
        }

        System.out.println("------------------------------------");
        // Example 4: Multiple catch blocks
        try {
            Object obj = "Hello";
            // Integer number = (Integer) obj; // ClassCastException
            
            int[] arr = new int[5];
            arr[10] = 50; // ArrayIndexOutOfBoundsException

        } catch (ClassCastException e) {
            System.err.println("Caught ClassCastException: " + e.getMessage());
        } catch (ArrayIndexOutOfBoundsException e) {
            System.err.println("Caught ArrayIndexOutOfBoundsException: " + e.getMessage());
        } catch (Exception e) { // Generic catch block (should be last)
            System.err.println("Caught a generic exception: " + e.getMessage());
        }

        System.out.println("Program continues after exception handling.");
    }
}
```

#### 2. How to create user-defined exceptions
You can create your own custom exception classes by extending the `Exception` class (for checked exceptions) or the `RuntimeException` class (for unchecked exceptions).

**Steps to create a user-defined exception:**
1.  Create a new class that extends `java.lang.Exception` or one of its subclasses.
2.  It's good practice to provide constructors that mirror the constructors of the `Exception` class, especially one that takes a `String` message.

**Example:**

```java
// Custom checked exception
class InsufficientFundsException extends Exception {
    private double amount;

    public InsufficientFundsException(String message, double amount) {
        super(message); // Call superclass (Exception) constructor
        this.amount = amount;
    }

    public InsufficientFundsException(String message) {
        super(message);
    }

    public double getAmount() {
        return amount;
    }
}

// Custom unchecked exception
class InvalidAgeException extends RuntimeException {
    public InvalidAgeException(String message) {
        super(message);
    }
}

class BankAccount {
    private double balance;

    public BankAccount(double initialBalance) {
        this.balance = initialBalance;
    }

    public void deposit(double amount) {
        if (amount <= 0) {
            throw new IllegalArgumentException("Deposit amount must be positive.");
        }
        balance += amount;
        System.out.println(amount + " deposited. Current balance: " + balance);
    }

    public void withdraw(double amount) throws InsufficientFundsException {
        if (amount <= 0) {
            throw new IllegalArgumentException("Withdrawal amount must be positive.");
        }
        if (amount > balance) {
            throw new InsufficientFundsException("Insufficient funds to withdraw " + amount + ". Available balance: " + balance, amount);
        }
        balance -= amount;
        System.out.println(amount + " withdrawn. Current balance: " + balance);
    }

    public double getBalance() {
        return balance;
    }
}

public class UserDefinedExceptionExample {
    public static void validateAge(int age) {
        if (age < 18) {
            throw new InvalidAgeException("User is underage. Age: " + age);
        } else {
            System.out.println("Age is valid.");
        }
    }

    public static void main(String[] args) {
        BankAccount account = new BankAccount(1000);

        try {
            account.deposit(500);
            account.withdraw(200);
            account.withdraw(1500); // This will throw InsufficientFundsException
        } catch (InsufficientFundsException e) {
            System.err.println("Error: " + e.getMessage());
            System.err.println("Requested withdrawal amount: " + e.getAmount());
        } catch (IllegalArgumentException e) {
            System.err.println("Error: " + e.getMessage());
        }

        System.out.println("------------------------------------");

        try {
            validateAge(25);
            validateAge(16); // This will throw InvalidAgeException
        } catch (InvalidAgeException e) {
            System.err.println("Age validation error: " + e.getMessage());
        }

        System.out.println("Program finished.");
    }
}
```

#### 3. Polymorphism: Method Overloading, Overriding, Dynamic Method Dispatch

Polymorphism ("many forms") is a core OOP concept that allows objects of different classes to be treated as objects of a common superclass. It enables performing a single action in different ways.

*   **Method Overloading (Compile-time Polymorphism / Static Binding):**
    *   Occurs when two or more methods within the same class have the same name but different parameter lists (different number of parameters, different types of parameters, or different order of parameters).
    *   The compiler decides which method to call at compile time based on the method signature (name and parameter list).
    *   Return type alone is not sufficient to overload a method.

    ```java
    class MathOperations {
        // Overloaded sum method
        public int sum(int a, int b) {
            System.out.println("sum(int, int) called");
            return a + b;
        }

        public double sum(double a, double b) {
            System.out.println("sum(double, double) called");
            return a + b;
        }

        public int sum(int a, int b, int c) {
            System.out.println("sum(int, int, int) called");
            return a + b + c;
        }

        public String sum(String s1, String s2) {
            System.out.println("sum(String, String) called");
            return s1 + s2;
        }
    }

    public class MethodOverloadingExample {
        public static void main(String[] args) {
            MathOperations ops = new MathOperations();

            System.out.println("Sum 1: " + ops.sum(5, 10));
            System.out.println("Sum 2: " + ops.sum(3.5, 2.5));
            System.out.println("Sum 3: " + ops.sum(1, 2, 3));
            System.out.println("Sum 4: " + ops.sum("Hello, ", "World!"));
        }
    }
    ```

*   **Method Overriding (Run-time Polymorphism / Dynamic Binding):**
    *   Occurs when a subclass provides a specific implementation for a method that is already defined in its superclass.
    *   The method in the subclass must have the same name, same parameter list, and same return type (or a subtype, known as covariant return type) as the method in the superclass.
    *   The `@Override` annotation is recommended to ensure the method is correctly overridden.
    *   The decision of which method to execute (superclass's or subclass's) is made at runtime based on the actual type of the object.

    ```java
    class AnimalSound {
        public void makeSound() {
            System.out.println("Animal makes a generic sound");
        }
    }

    class DogSound extends AnimalSound {
        @Override // Good practice
        public void makeSound() {
            System.out.println("Dog barks: Woof woof!");
        }
        public void specificDogMethod() {
            System.out.println("This is a specific dog method.");
        }
    }

    class CatSound extends AnimalSound {
        @Override
        public void makeSound() {
            System.out.println("Cat meows: Meow!");
        }
    }

    public class MethodOverridingExample {
        public static void main(String[] args) {
            AnimalSound myAnimal = new AnimalSound();
            myAnimal.makeSound(); // Calls AnimalSound's makeSound

            AnimalSound myDog = new DogSound(); // Superclass reference, subclass object
            myDog.makeSound();    // Calls DogSound's makeSound (runtime polymorphism)
            // myDog.specificDogMethod(); // Error: AnimalSound reference doesn't know this method

            DogSound actualDog = new DogSound();
            actualDog.specificDogMethod(); // This is fine

            AnimalSound myCat = new CatSound();
            myCat.makeSound();    // Calls CatSound's makeSound
        }
    }
    ```

*   **Dynamic Method Dispatch:**
    *   This is the mechanism by which a call to an overridden method is resolved at runtime rather than compile time.
    *   It's how Java implements runtime polymorphism with method overriding.
    *   When an overridden method is called through a superclass reference variable, Java determines which version of that method to execute (the one in the superclass or the one in the subclass) based on the type of the object being referred to at the moment the call occurs.

    **Example (same as MethodOverridingExample, highlighting dynamic dispatch):**
    ```java
    // (AnimalSound, DogSound, CatSound classes from above)

    public class DynamicMethodDispatchExample {
        public static void main(String[] args) {
            AnimalSound ref; // Superclass reference

            ref = new AnimalSound();
            ref.makeSound(); // Calls AnimalSound.makeSound()

            ref = new DogSound();    // ref now points to a DogSound object
            ref.makeSound(); // Dynamically dispatches to DogSound.makeSound() at runtime

            ref = new CatSound();    // ref now points to a CatSound object
            ref.makeSound(); // Dynamically dispatches to CatSound.makeSound() at runtime
        }
    }
    ```
    In this example, the `ref.makeSound()` call invokes different methods depending on the actual object `ref` is pointing to at runtime. This is dynamic method dispatch.

---
### Unit 3: Multithreading & I/O, Collections

#### 1. What is Multithreading and how to create a thread
**Multithreading** is a concurrency mechanism that allows multiple parts of a program (called threads) to run concurrently. Each thread is a lightweight sub-process, an independent path of execution within a program. Multithreading can improve the performance and responsiveness of applications, especially for tasks that can be broken down into smaller, independent units of work.

**Benefits of Multithreading:**
*   **Improved Performance:** Multiple threads can execute in parallel on multi-core processors.
*   **Responsiveness:** Keeps the application responsive, especially in GUI applications where one thread can handle user interaction while another performs background tasks.
*   **Resource Sharing:** Threads within the same process share the same memory space, allowing for efficient communication and data sharing.
*   **Reduced Development Time (for certain problems):** Complex tasks can be broken down.

**Ways to Create a Thread in Java:**

1.  **By Extending the `Thread` Class:**
    *   Create a new class that extends `java.lang.Thread`.
    *   Override the `run()` method in your class. This method contains the code that will be executed by the new thread.
    *   Create an instance of your new class.
    *   Call the `start()` method on the instance. This will cause the JVM to call the `run()` method.

    ```java
    class MyThread extends Thread {
        private String threadName;

        public MyThread(String name) {
            this.threadName = name;
            System.out.println("Creating " +  threadName );
        }

        @Override
        public void run() {
            System.out.println("Running " +  threadName );
            try {
                for(int i = 4; i > 0; i--) {
                    System.out.println("Thread: " + threadName + ", " + i);
                    // Let the thread sleep for a while.
                    Thread.sleep(50);
                }
            } catch (InterruptedException e) {
                System.out.println("Thread " +  threadName + " interrupted.");
            }
            System.out.println("Thread " +  threadName + " exiting.");
        }
    }

    public class ExtendThreadExample {
        public static void main(String args[]) {
            MyThread thread1 = new MyThread("Thread-1-Extends");
            thread1.start(); // Calls run() method

            MyThread thread2 = new MyThread("Thread-2-Extends");
            thread2.start(); // Calls run() method
        }
    }
    ```

2.  **By Implementing the `Runnable` Interface:**
    *   Create a new class that implements the `java.lang.Runnable` interface.
    *   Implement the `run()` method in your class.
    *   Create an instance of your new class.
    *   Create an instance of the `Thread` class, passing your `Runnable` object to its constructor.
    *   Call the `start()` method on the `Thread` instance.

    This approach is generally preferred because Java does not support multiple inheritance of classes. If your class already extends another class, it cannot also extend `Thread`. Implementing `Runnable` allows for more flexibility.

    ```java
    class MyRunnable implements Runnable {
        private String threadName;
        private Thread t;

        public MyRunnable(String name) {
            this.threadName = name;
            System.out.println("Creating " +  threadName );
        }

        @Override
        public void run() {
            System.out.println("Running " +  threadName );
            try {
                for(int i = 4; i > 0; i--) {
                    System.out.println("Thread: " + threadName + ", " + i);
                    Thread.sleep(50);
                }
            } catch (InterruptedException e) {
                System.out.println("Thread " +  threadName + " interrupted.");
            }
            System.out.println("Thread " +  threadName + " exiting.");
        }

        public void start() {
            System.out.println("Starting " +  threadName );
            if (t == null) {
                t = new Thread(this, threadName); // Pass Runnable instance to Thread constructor
                t.start();
            }
        }
    }

    public class ImplementRunnableExample {
        public static void main(String args[]) {
            MyRunnable runnable1 = new MyRunnable("Thread-1-Runnable");
            runnable1.start();

            MyRunnable runnable2 = new MyRunnable("Thread-2-Runnable");
            runnable2.start();
        }
    }
    ```

#### 2. Synchronized method and synchronized blocks
When multiple threads access shared resources (variables or objects), it can lead to data inconsistency and race conditions. Synchronization is a mechanism to control the access of multiple threads to any shared resource. Java provides synchronization using the `synchronized` keyword.

*   **Synchronized Method:**
    *   When a method is declared as `synchronized`, only one thread can execute that method on a given instance of the class at a time.
    *   If a thread is executing a synchronized method, any other thread trying to execute *any* synchronized method on the *same object* will be blocked until the first thread releases the object's monitor (lock).
    *   The lock is acquired on the `this` object for instance methods, and on the `.class` object for static synchronized methods.

    ```java
    class Counter {
        private int count = 0;

        // Synchronized method
        public synchronized void increment() {
            count++;
        }

        public synchronized int getCount() {
            return count;
        }
    }

    class SyncMethodThread extends Thread {
        private Counter counter;
        public SyncMethodThread(Counter counter, String name) {
            super(name);
            this.counter = counter;
        }
        @Override
        public void run() {
            for (int i = 0; i < 10000; i++) {
                counter.increment();
            }
            System.out.println(Thread.currentThread().getName() + " finished. Count: " + counter.getCount());
        }
    }

    public class SynchronizedMethodExample {
        public static void main(String[] args) throws InterruptedException {
            Counter sharedCounter = new Counter();

            SyncMethodThread t1 = new SyncMethodThread(sharedCounter, "Thread-A");
            SyncMethodThread t2 = new SyncMethodThread(sharedCounter, "Thread-B");

            t1.start();
            t2.start();

            t1.join(); // Wait for t1 to finish
            t2.join(); // Wait for t2 to finish

            System.out.println("Final count: " + sharedCounter.getCount()); // Expected: 20000
        }
    }
    ```

*   **Synchronized Block:**
    *   Provides finer-grained control over synchronization. Instead of locking the entire method, you can lock only a specific part of the code that accesses the shared resource.
    *   The `synchronized` keyword is used with an object reference: `synchronized(objectReference) { // critical section }`.
    *   The thread acquires a lock on the `objectReference` before executing the block.
    *   This can improve performance if the critical section is small compared to the entire method.
    *   You can synchronize on `this` (current object), any other object, or a class literal (`ClassName.class` for static context).

    ```java
    class MessageSender {
        public void send(String msg) {
            System.out.println("Sending\t" + msg);
            try {
                Thread.sleep(1000); // Simulate time taken to send
            } catch (Exception e) {
                System.out.println("Thread interrupted.");
            }
            System.out.println("\n" + msg + "Sent");
        }
    }

    class SyncBlockThread extends Thread {
        private String msg;
        private MessageSender sender; // Shared object
        private Object lockObject; // Can be any shared object for locking

        // Constructor using 'this' for synchronization on sender object
        public SyncBlockThread(String m, MessageSender obj) {
            msg = m;
            sender = obj;
            this.lockObject = sender; // Synchronize on the sender object itself
        }
        
        // Constructor using a dedicated lock object
        public SyncBlockThread(String m, MessageSender obj, Object lock) {
            msg = m;
            sender = obj;
            this.lockObject = lock;
        }


        @Override
        public void run() {
            // Synchronize on the lockObject
            // Only one thread can execute this block on the 'lockObject' at a time.
            synchronized (lockObject) {
                sender.send(msg);
            }
        }
    }

    public class SynchronizedBlockExample {
        public static void main(String args[]) {
            MessageSender commonSender = new MessageSender();
            Object dedicatedLock = new Object(); // A dedicated object for locking

            // Scenario 1: Synchronizing on the shared 'commonSender' object
            System.out.println("--- Scenario 1: Synchronizing on commonSender object ---");
            SyncBlockThread senderThread1 = new SyncBlockThread("Hi from Thread1", commonSender);
            SyncBlockThread senderThread2 = new SyncBlockThread("Bye from Thread2", commonSender);
            
            senderThread1.start();
            senderThread2.start();

            try {
                senderThread1.join();
                senderThread2.join();
            } catch (Exception e) {
                System.out.println("Interrupted");
            }
            
            System.out.println("\n--- Scenario 2: Synchronizing on a dedicated lock object ---");
            MessageSender anotherSender = new MessageSender(); // Different sender, but could be same
            SyncBlockThread senderThread3 = new SyncBlockThread("Hello from Thread3", anotherSender, dedicatedLock);
            SyncBlockThread senderThread4 = new SyncBlockThread("Greetings from Thread4", anotherSender, dedicatedLock);

            senderThread3.start();
            senderThread4.start();
            
            try {
                senderThread3.join();
                senderThread4.join();
            } catch (Exception e) {
                System.out.println("Interrupted");
            }
        }
    }
    ```

#### 3. Inter-thread communication and methods: `wait()`, `notify()`, `notifyAll()`
Inter-thread communication allows threads to communicate with each other, typically to coordinate their activities. Java provides `wait()`, `notify()`, and `notifyAll()` methods (defined in the `Object` class) for this purpose. These methods must be called from within a synchronized block or method, on the object whose lock is held.

*   **`wait()`**:
    *   Causes the current thread to release the lock on the object and enter a waiting state until another thread invokes `notify()` or `notifyAll()` on the same object, or until a specified timeout occurs.
    *   `wait()`: Waits indefinitely.
    *   `wait(long timeout)`: Waits for a specified amount of time (in milliseconds).
    *   `wait(long timeout, int nanos)`: Waits for a specified amount of time (milliseconds + nanoseconds).
*   **`notify()`**:
    *   Wakes up a single thread that is waiting on this object's monitor. If multiple threads are waiting, one is chosen arbitrarily.
*   **`notifyAll()`**:
    *   Wakes up all threads that are waiting on this object's monitor.

**Example: Producer-Consumer Problem**

```java
import java.util.LinkedList;
import java.util.Queue;

class SharedBuffer {
    private Queue<Integer> buffer;
    private int capacity;

    public SharedBuffer(int capacity) {
        this.buffer = new LinkedList<>();
        this.capacity = capacity;
    }

    // Producer method
    public synchronized void produce(int item) throws InterruptedException {
        // Wait if the buffer is full
        while (buffer.size() == capacity) {
            System.out.println("Buffer is full. Producer " + Thread.currentThread().getName() + " is waiting...");
            wait(); // Releases the lock and waits
        }

        buffer.add(item);
        System.out.println("Producer " + Thread.currentThread().getName() + " produced: " + item + ". Buffer size: " + buffer.size());

        // Notify a waiting consumer (if any)
        notifyAll(); // Wakes up one or all waiting threads (consumers in this case)
    }

    // Consumer method
    public synchronized int consume() throws InterruptedException {
        // Wait if the buffer is empty
        while (buffer.isEmpty()) {
            System.out.println("Buffer is empty. Consumer " + Thread.currentThread().getName() + " is waiting...");
            wait(); // Releases the lock and waits
        }

        int item = buffer.poll();
        System.out.println("Consumer " + Thread.currentThread().getName() + " consumed: " + item + ". Buffer size: " + buffer.size());

        // Notify a waiting producer (if any)
        notifyAll(); // Wakes up one or all waiting threads (producers in this case)
        return item;
    }
}

class Producer implements Runnable {
    private SharedBuffer sharedBuffer;
    public Producer(SharedBuffer sharedBuffer) {
        this.sharedBuffer = sharedBuffer;
    }
    @Override
    public void run() {
        for (int i = 1; i <= 5; i++) {
            try {
                sharedBuffer.produce(i);
                Thread.sleep((long) (Math.random() * 100)); // Simulate work
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
                System.err.println("Producer interrupted");
            }
        }
    }
}

class Consumer implements Runnable {
    private SharedBuffer sharedBuffer;
    public Consumer(SharedBuffer sharedBuffer) {
        this.sharedBuffer = sharedBuffer;
    }
    @Override
    public void run() {
        for (int i = 1; i <= 5; i++) {
            try {
                sharedBuffer.consume();
                Thread.sleep((long) (Math.random() * 200)); // Simulate work
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
                System.err.println("Consumer interrupted");
            }
        }
    }
}

public class InterThreadCommunicationExample {
    public static void main(String[] args) {
        SharedBuffer buffer = new SharedBuffer(2); // Buffer capacity of 2

        Thread producerThread1 = new Thread(new Producer(buffer), "P1");
        Thread producerThread2 = new Thread(new Producer(buffer), "P2");
        Thread consumerThread1 = new Thread(new Consumer(buffer), "C1");
        Thread consumerThread2 = new Thread(new Consumer(buffer), "C2");

        producerThread1.start();
        consumerThread1.start();
        producerThread2.start();
        consumerThread2.start();

        try {
            producerThread1.join();
            producerThread2.join();
            consumerThread1.join();
            consumerThread2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println("Main thread finished.");
    }
}
```

#### 4. Types of Java I/O: Byte Streams and Character Streams, and examples for each class
Java I/O (Input/Output) is handled through streams. A stream is a sequence of data.
There are two main types of streams:

*   **Byte Streams:**
    *   Handle I/O of raw binary data (8-bit bytes).
    *   Suitable for reading/writing binary files like images, audio, video, or any type of file where character encoding is not relevant or needs to be handled at a lower level.
    *   Base abstract classes: `InputStream` and `OutputStream`.
    *   **Key Concrete Classes:**
        *   `FileInputStream` / `FileOutputStream`: For reading from and writing to files.
        *   `ByteArrayInputStream` / `ByteArrayOutputStream`: For reading from and writing to byte arrays in memory.
        *   `BufferedInputStream` / `BufferedOutputStream`: Add buffering for improved performance.
        *   `DataInputStream` / `DataOutputStream`: For reading/writing Java primitive data types in a platform-independent way.
        *   `ObjectInputStream` / `ObjectOutputStream`: For serializing and deserializing objects.

*   **Character Streams:**
    *   Handle I/O of character data (16-bit Unicode characters).
    *   Automatically handle character encoding conversion (e.g., UTF-8, ASCII).
    *   Suitable for reading/writing text files.
    *   Base abstract classes: `Reader` and `Writer`.
    *   **Key Concrete Classes:**
        *   `FileReader` / `FileWriter`: For reading from and writing to text files.
        *   `CharArrayReader` / `CharArrayWriter`: For reading from and writing to char arrays in memory.
        *   `BufferedReader` / `BufferedWriter`: Add buffering for improved performance, and `BufferedReader` provides `readLine()` method.
        *   `InputStreamReader` / `OutputStreamWriter`: Bridges between byte streams and character streams. `InputStreamReader` reads bytes and decodes them into characters using a specified charset. `OutputStreamWriter` takes characters and encodes them into bytes.

**Example: Byte Streams (`FileInputStream` and `FileOutputStream`)**

```java
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class ByteStreamExample {
    public static void main(String[] args) {
        String inputFile = "input_byte.dat"; // Create this file with some content
        String outputFile = "output_byte.dat";

        // Create a sample input file
        try (FileOutputStream fosTemp = new FileOutputStream(inputFile)) {
            fosTemp.write(new byte[]{72, 101, 108, 108, 111}); // "Hello"
        } catch (IOException e) {
            System.err.println("Error creating sample input file: " + e.getMessage());
            return;
        }


        // Using try-with-resources to ensure streams are closed automatically
        try (FileInputStream fis = new FileInputStream(inputFile);
             FileOutputStream fos = new FileOutputStream(outputFile)) {

            int byteData;
            // Read byte by byte from input stream and write to output stream
            while ((byteData = fis.read()) != -1) { // read() returns -1 at EOF
                fos.write(byteData);
            }
            System.out.println("Byte stream copy complete. Check " + outputFile);

        } catch (IOException e) {
            System.err.println("An I/O error occurred: " + e.getMessage());
            e.printStackTrace();
        }
    }
}
```

**Example: Character Streams (`FileReader` and `FileWriter`, `BufferedReader`, `BufferedWriter`)**

```java
import java.io.FileReader;
import java.io.FileWriter;
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;

public class CharacterStreamExample {
    public static void main(String[] args) {
        String inputFile = "input_char.txt"; // Create this file with some text
        String outputFile = "output_char.txt";

        // Create a sample input file
        try (FileWriter fwTemp = new FileWriter(inputFile)) {
            fwTemp.write("Hello Java World!\nThis is a test.\nLine 3.");
        } catch (IOException e) {
            System.err.println("Error creating sample input file: " + e.getMessage());
            return;
        }

        // Using try-with-resources
        try (FileReader fr = new FileReader(inputFile);
             FileWriter fw = new FileWriter(outputFile)) {

            int charData;
            // Read character by character
            while ((charData = fr.read()) != -1) { // read() returns -1 at EOF
                fw.write(charData);
            }
            System.out.println("Character stream copy (char by char) complete. Check " + outputFile);

        } catch (IOException e) {
            System.err.println("An I/O error occurred (char by char): " + e.getMessage());
        }

        // Using BufferedReader and BufferedWriter for efficiency (line by line)
        String outputFileBuffered = "output_char_buffered.txt";
        try (BufferedReader br = new BufferedReader(new FileReader(inputFile));
             BufferedWriter bw = new BufferedWriter(new FileWriter(outputFileBuffered))) {

            String line;
            while ((line = br.readLine()) != null) {
                bw.write(line);
                bw.newLine(); // Writes a platform-dependent line separator
            }
            System.out.println("Character stream copy (buffered line by line) complete. Check " + outputFileBuffered);

        } catch (IOException e) {
            System.err.println("An I/O error occurred (buffered): " + e.getMessage());
        }
    }
}
```

#### 5. `LinkedList`, `HashSet`, `ArrayList` (mostly theory)
These are part of the Java Collections Framework, found in the `java.util` package.

*   **`ArrayList`**
    *   **Implementation:** Implements the `List` interface. Internally uses a dynamic array to store elements.
    *   **Ordering:** Maintains the insertion order of elements. Elements are accessed by their integer index (position).
    *   **Duplicates:** Allows duplicate elements.
    *   **Nulls:** Allows multiple null values.
    *   **Performance:**
        *   Fast for random access (getting an element by index, `get(index)`) because it's array-based (O(1) time complexity).
        *   Slower for insertion and deletion in the middle of the list (O(n) time complexity) because it may require shifting elements. Adding to the end is generally O(1) amortized, unless the internal array needs resizing.
    *   **Synchronization:** Not synchronized by default. If thread-safety is needed, use `Collections.synchronizedList(new ArrayList<>())` or `CopyOnWriteArrayList`.
    *   **Use Cases:** Good choice when you need fast random access and the number of insertions/deletions is relatively low, or insertions/deletions happen mostly at the end.

*   **`LinkedList`**
    *   **Implementation:** Implements the `List` and `Deque` (Double Ended Queue) interfaces. Internally uses a doubly-linked list (each element has a reference to the previous and next element).
    *   **Ordering:** Maintains the insertion order of elements.
    *   **Duplicates:** Allows duplicate elements.
    *   **Nulls:** Allows multiple null values.
    *   **Performance:**
        *   Slower for random access (getting an element by index, `get(index)`) because it may require traversing part of the list (O(n) time complexity).
        *   Faster for insertion and deletion at the beginning or end of the list (O(1) time complexity), and generally faster for insertions/deletions in the middle compared to `ArrayList` if you have an iterator at the position, as it only involves updating links.
    *   **Synchronization:** Not synchronized by default. If thread-safety is needed, use `Collections.synchronizedList(new LinkedList<>())`.
    *   **Use Cases:** Good choice when you have frequent insertions and deletions, especially at the beginning or end. Also useful when you need queue or deque functionality (e.g., `addFirst()`, `removeLast()`).

*   **`HashSet`**
    *   **Implementation:** Implements the `Set` interface. Internally uses a hash table (specifically, a `HashMap` instance) for storage.
    *   **Ordering:** Does **not** guarantee any specific order of elements. The order may change over time. If you need insertion order, use `LinkedHashSet`. If you need sorted order, use `TreeSet`.
    *   **Duplicates:** Does **not** allow duplicate elements. If you try to add an element that is already present (based on `equals()` and `hashCode()` methods), the add operation is ignored.
    *   **Nulls:** Allows at most one null value.
    *   **Performance:**
        *   Offers constant time performance (O(1) on average) for basic operations like `add`, `remove`, `contains`, and `size`, assuming the hash function disperses elements properly among buckets.
        *   Performance can degrade to O(n) in the worst case (e.g., if all elements have the same hash code).
    *   **Synchronization:** Not synchronized by default. If thread-safety is needed, use `Collections.synchronizedSet(new HashSet<>())`.
    *   **Use Cases:** Good choice when you need to store a collection of unique items and don't care about their order, and when fast lookups (checking for existence) are important.

**Summary Table:**

| Feature          | `ArrayList`                      | `LinkedList`                     | `HashSet`                        |
|------------------|----------------------------------|----------------------------------|----------------------------------|
| **Interface**    | `List`                           | `List`, `Deque`                  | `Set`                            |
| **Internal DS**  | Dynamic Array                    | Doubly Linked List               | Hash Table (uses `HashMap`)      |
| **Ordering**     | Insertion Order                  | Insertion Order                  | No specific order (unordered)    |
| **Duplicates**   | Allowed                          | Allowed                          | Not Allowed                      |
| **Nulls**        | Multiple allowed                 | Multiple allowed                 | One null allowed                 |
| **Random Access**| Fast (O(1))                      | Slow (O(n))                      | N/A (no index)                   |
| **Add/Remove**   | Slow (O(n) mid), Fast (O(1) end) | Fast (O(1) ends/iterator)        | Fast (O(1) avg)                  |
| **`contains()`** | O(n)                             | O(n)                             | Fast (O(1) avg)                  |
| **Synchronization**| Not synchronized                 | Not synchronized                 | Not synchronized                 |

---
### Unit 4: AWT & Swings, Event Handling, JDBC

#### 1. AWT (Abstract Window Toolkit)
The Abstract Window Toolkit (AWT) is Java's original platform-dependent API for creating Graphical User Interfaces (GUIs). It provides a set of classes for creating windows, buttons, text fields, and other GUI components.

*   **Platform-Dependent:** AWT components are "heavyweight" components. This means they rely on the native GUI toolkit of the underlying operating system. For example, an AWT button on Windows looks like a Windows button, and on macOS, it looks like a macOS button.
*   **Package:** `java.awt`
*   **Key Components:**
    *   **Containers:** `Frame` (top-level window with title and border), `Panel` (generic container for organizing components), `Dialog` (pop-up window).
    *   **Components:** `Button`, `Label`, `TextField`, `TextArea`, `Checkbox`, `Choice` (drop-down list), `List`, `Scrollbar`, `Canvas`.
*   **Layout Managers:** AWT uses layout managers to arrange components within a container (e.g., `FlowLayout`, `BorderLayout`, `GridLayout`).
*   **Event Handling:** AWT uses an event delegation model (listeners and events) to respond to user interactions.
*   **Limitations:**
    *   Limited set of components compared to Swing.
    *   Platform-dependent look and feel can lead to inconsistencies across different OS.
    *   Heavyweight nature can sometimes lead to performance issues or conflicts with other windowing elements.

While Swing has largely superseded AWT for new GUI development due to its richer component set and pluggable look and feel, understanding AWT is important as Swing builds upon some AWT concepts and can mix AWT components (though generally not recommended).

```java
import java.awt.*;
import java.awt.event.*;

// Simple AWT Frame example
public class AwtExample extends Frame {

    public AwtExample(String title) {
        super(title); // Set frame title
        setLayout(new FlowLayout()); // Set layout manager

        Label label = new Label("This is an AWT Label:");
        TextField textField = new TextField("Enter text here", 20);
        Button button = new Button("Click Me (AWT)");

        // Add components to the frame
        add(label);
        add(textField);
        add(button);

        // Add an ActionListener to the button
        button.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                textField.setText("AWT Button Clicked!");
            }
        });

        // Add a WindowListener to handle closing the frame
        addWindowListener(new WindowAdapter() {
            @Override
            public void windowClosing(WindowEvent e) {
                System.out.println("AWT Frame is closing.");
                dispose(); // Release resources
                System.exit(0); // Terminate the application
            }
        });

        setSize(350, 150); // Set frame size
        setVisible(true);  // Make frame visible
    }

    public static void main(String[] args) {
        new AwtExample("My AWT Application");
    }
}
```

#### 2. Layouts (AWT/Swing)
Layout managers are responsible for arranging components within a container. They determine the size and position of components. Using layout managers makes GUIs more portable across different screen sizes and resolutions.

Common Layout Managers (available in both AWT and Swing):

*   **`FlowLayout`:**
    *   Arranges components in a directional flow, much like lines of text in a paragraph.
    *   Components are added left-to-right, top-to-bottom. When a row is filled, a new row is started.
    *   Default layout for `Panel` and `Applet`.
    *   Alignment can be `LEFT`, `CENTER` (default), or `RIGHT`.
    ```java
    // panel.setLayout(new FlowLayout(FlowLayout.LEFT, 10, 5)); // Align left, hgap=10, vgap=5
    ```

*   **`BorderLayout`:**
    *   Divides the container into five regions: `NORTH`, `SOUTH`, `EAST`, `WEST`, and `CENTER`.
    *   Each region can hold at most one component.
    *   Components in `NORTH` and `SOUTH` get their preferred height and the full width of the container.
    *   Components in `EAST` and `WEST` get their preferred width and the height remaining after `NORTH` and `SOUTH`.
    *   The `CENTER` component takes up any remaining space.
    *   Default layout for `Frame`, `JFrame`, `Dialog`, `JDialog`.
    ```java
    // frame.add(new Button("North"), BorderLayout.NORTH);
    // frame.add(new Button("Center"), BorderLayout.CENTER);
    ```

*   **`GridLayout`:**
    *   Arranges components in a rectangular grid of equal-sized cells.
    *   Components are added row by row, left to right.
    *   You specify the number of rows and columns.
    ```java
    // panel.setLayout(new GridLayout(3, 2, 5, 5)); // 3 rows, 2 columns, hgap=5, vgap=5
    // panel.add(new Button("1")); panel.add(new Button("2")); ...
    ```

*   **`CardLayout`:**
    *   Manages multiple components (cards) where only one is visible at a time.
    *   Useful for creating wizards or tab-like interfaces without actual tabs.
    *   You can switch between cards programmatically.
    ```java
    // CardLayout cardLayout = new CardLayout();
    // JPanel cardPanel = new JPanel(cardLayout);
    // cardPanel.add(panel1, "Card1");
    // cardPanel.add(panel2, "Card2");
    // cardLayout.show(cardPanel, "Card2"); // Show Card2
    ```

*   **`GridBagLayout`:**
    *   The most flexible and complex layout manager.
    *   Arranges components in a grid of cells, but cells can have different sizes, and components can span multiple cells.
    *   Uses `GridBagConstraints` to specify placement, size, and behavior of each component.
    *   Powerful but can be challenging to use directly.

*   **`BoxLayout` (Swing specific, but similar concept can be achieved in AWT):**
    *   Arranges components in a single row (`X_AXIS`) or a single column (`Y_AXIS`).
    *   Respects component's maximum, minimum, and preferred sizes.
    *   Often used with `Box` container for easy spacing (struts, glue).

**Example using `BorderLayout` and `GridLayout` (Swing):**
```java
import javax.swing.*;
import java.awt.*;

public class LayoutManagerSwingExample {
    public static void main(String[] args) {
        JFrame frame = new JFrame("Layout Manager Demo (Swing)");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(400, 300);

        // Main panel using BorderLayout
        JPanel mainPanel = new JPanel(new BorderLayout(5, 5)); // Gaps

        // Components for BorderLayout
        JButton northButton = new JButton("NORTH");
        JButton southButton = new JButton("SOUTH");
        JButton eastButton = new JButton("EAST");
        JButton westButton = new JButton("WEST");

        // Panel for the center using GridLayout
        JPanel centerPanel = new JPanel(new GridLayout(2, 2, 10, 10)); // 2x2 grid, gaps
        centerPanel.add(new JButton("Cell 1"));
        centerPanel.add(new JButton("Cell 2"));
        centerPanel.add(new JButton("Cell 3"));
        centerPanel.add(new JButton("Cell 4"));
        centerPanel.setBorder(BorderFactory.createTitledBorder("Center Panel (GridLayout)"));


        mainPanel.add(northButton, BorderLayout.NORTH);
        mainPanel.add(southButton, BorderLayout.SOUTH);
        mainPanel.add(eastButton, BorderLayout.EAST);
        mainPanel.add(westButton, BorderLayout.WEST);
        mainPanel.add(centerPanel, BorderLayout.CENTER);

        frame.add(mainPanel);
        frame.setVisible(true);
    }
}
```

#### 3. GUI Components: `Label`, `Checkbox`, etc. (Swing examples)
Swing provides a richer set of GUI components than AWT. Swing components are "lightweight" (written purely in Java) and offer a pluggable look and feel. Most Swing components start with `J` (e.g., `JButton`, `JLabel`).

*   **`JLabel`**: Displays a non-editable text string or an image.
    ```java
    JLabel label = new JLabel("Enter your name:");
    JLabel imageLabel = new JLabel(new ImageIcon("path/to/image.png"));
    ```
*   **`JButton`**: A clickable button that can trigger an action.
    ```java
    JButton button = new JButton("Submit");
    button.addActionListener(e -> System.out.println("Button clicked!"));
    ```
*   **`JTextField`**: A single-line text input field.
    ```java
    JTextField nameField = new JTextField(20); // 20 columns wide
    String text = nameField.getText();
    nameField.setText("Default Text");
    ```
*   **`JTextArea`**: A multi-line text input/output area.
    ```java
    JTextArea descriptionArea = new JTextArea(5, 30); // 5 rows, 30 columns
    descriptionArea.setLineWrap(true);
    descriptionArea.setWrapStyleWord(true);
    JScrollPane scrollPane = new JScrollPane(descriptionArea); // Often used with JScrollPane
    ```
*   **`JCheckBox`**: A checkbox that can be selected or deselected.
    ```java
    JCheckBox agreeCheckBox = new JCheckBox("I agree to the terms.");
    boolean isSelected = agreeCheckBox.isSelected();
    agreeCheckBox.setSelected(true);
    ```
*   **`JRadioButton`**: A radio button, typically used in a `ButtonGroup` to allow only one selection among a group.
    ```java
    JRadioButton maleRadio = new JRadioButton("Male");
    JRadioButton femaleRadio = new JRadioButton("Female");
    ButtonGroup genderGroup = new ButtonGroup();
    genderGroup.add(maleRadio);
    genderGroup.add(femaleRadio);
    maleRadio.setSelected(true); // Default selection
    ```
*   **`JComboBox` (Dropdown/Choice)**: A drop-down list of items from which the user can select one.
    ```java
    String[] countries = {"USA", "Canada", "UK", "India"};
    JComboBox<String> countryComboBox = new JComboBox<>(countries);
    String selectedCountry = (String) countryComboBox.getSelectedItem();
    countryComboBox.addItem("Germany");
    ```
*   **`JList`**: Displays a list of items from which one or more can be selected.
    ```java
    String[] fruits = {"Apple", "Banana", "Orange", "Mango"};
    JList<String> fruitList = new JList<>(fruits);
    fruitList.setSelectionMode(ListSelectionModel.SINGLE_SELECTION); // or MULTIPLE_INTERVAL_SELECTION
    JScrollPane listScrollPane = new JScrollPane(fruitList);
    ```
*   **`JPanel`**: A generic lightweight container used to organize and group components.
*   **`JFrame`**: A top-level window with a title, border, and standard window controls.

**Example Program with various Swing Components:**
```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class SwingComponentsDemo {
    public static void main(String[] args) {
        JFrame frame = new JFrame("Swing Components Demo");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(400, 350);
        frame.setLayout(new FlowLayout(FlowLayout.LEFT, 10, 10));

        // JLabel and JTextField
        frame.add(new JLabel("Name:"));
        JTextField nameField = new JTextField(15);
        frame.add(nameField);

        // JCheckBox
        JCheckBox termsCheckBox = new JCheckBox("Agree to terms");
        frame.add(termsCheckBox);

        // JRadioButtons with ButtonGroup
        frame.add(new JLabel("Gender:"));
        JRadioButton maleRadio = new JRadioButton("Male");
        JRadioButton femaleRadio = new JRadioButton("Female");
        ButtonGroup genderGroup = new ButtonGroup();
        genderGroup.add(maleRadio);
        genderGroup.add(femaleRadio);
        maleRadio.setSelected(true);
        JPanel radioPanel = new JPanel(); // Use a panel to group radio buttons
        radioPanel.add(maleRadio);
        radioPanel.add(femaleRadio);
        frame.add(radioPanel);


        // JComboBox
        frame.add(new JLabel("Country:"));
        String[] countries = {"USA", "Canada", "UK", "India", "Other"};
        JComboBox<String> countryComboBox = new JComboBox<>(countries);
        frame.add(countryComboBox);

        // JTextArea with JScrollPane
        frame.add(new JLabel("Comments:"));
        JTextArea commentsArea = new JTextArea(3, 20);
        commentsArea.setLineWrap(true);
        JScrollPane scrollPane = new JScrollPane(commentsArea);
        frame.add(scrollPane);

        // JButton
        JButton submitButton = new JButton("Submit");
        frame.add(submitButton);

        // Output area
        JTextArea outputArea = new JTextArea(4, 30);
        outputArea.setEditable(false);
        frame.add(new JScrollPane(outputArea));

        // ActionListener for the button
        submitButton.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                StringBuilder sb = new StringBuilder();
                sb.append("Name: ").append(nameField.getText()).append("\n");
                sb.append("Agreed to terms: ").append(termsCheckBox.isSelected()).append("\n");
                String gender = maleRadio.isSelected() ? "Male" : "Female";
                sb.append("Gender: ").append(gender).append("\n");
                sb.append("Country: ").append(countryComboBox.getSelectedItem()).append("\n");
                sb.append("Comments: ").append(commentsArea.getText()).append("\n");
                outputArea.setText(sb.toString());
            }
        });

        frame.setVisible(true);
    }
}
```

#### 4. Event Delegation Model: Events, Event Sources, Event Listeners
The Event Delegation Model is the standard mechanism for handling events in Java GUIs (both AWT and Swing). It consists of three main components:

1.  **Event Source:**
    *   The object that generates or fires an event.
    *   Examples: A `JButton` (source of `ActionEvent`), a `JTextField` (source of `ActionEvent` on Enter, `KeyEvent`), a `JFrame` (source of `WindowEvent`).
    *   Sources maintain a list of listeners interested in their events.
    *   They provide methods to register (`addXxxListener()`) and unregister (`removeXxxListener()`) listeners.

2.  **Event Object (Event):**
    *   An object that encapsulates information about an event that has occurred.
    *   Contains details like the source of the event, type of event, and other event-specific data (e.g., mouse coordinates for a `MouseEvent`, key code for a `KeyEvent`).
    *   All event objects are subclasses of `java.util.EventObject`. GUI events are typically subclasses of `java.awt.AWTEvent`.
    *   Examples: `ActionEvent`, `MouseEvent`, `KeyEvent`, `WindowEvent`, `ItemEvent`.

3.  **Event Listener:**
    *   An object that is interested in receiving and processing events from a source.
    *   It implements a specific listener interface corresponding to the type of event it wants to handle.
    *   Listener interfaces define methods that are called when the event occurs.
    *   Examples:
        *   `ActionListener` (for `ActionEvent`): `actionPerformed(ActionEvent e)`
        *   `MouseListener` (for mouse clicks, presses, releases, enters, exits): `mouseClicked()`, `mousePressed()`, etc.
        *   `KeyListener` (for key presses, releases, typed): `keyPressed()`, `keyReleased()`, `keyTyped()`
        *   `WindowListener` (for window events like opening, closing): `windowOpened()`, `windowClosing()`, etc.

**How it Works:**
1.  An Event Listener object is created.
2.  The listener is registered with an Event Source (e.g., `button.addActionListener(myListener);`).
3.  When an event occurs on the source (e.g., user clicks the button), the source creates an Event Object.
4.  The source then invokes the appropriate method on all its registered listeners, passing the Event Object as an argument.
5.  The listener's method executes the code to handle the event.

**Example: Button Click Handling**
```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

// 1. Implement the ActionListener interface (or use an anonymous inner class / lambda)
class MyButtonClickListener implements ActionListener {
    private JLabel statusLabel;

    public MyButtonClickListener(JLabel label) {
        this.statusLabel = label;
    }

    @Override
    public void actionPerformed(ActionEvent e) { // This method is called when the event occurs
        // e is the Event Object (ActionEvent)
        // e.getSource() would return the button that was clicked
        statusLabel.setText("Button was clicked! Source: " + e.getActionCommand());
    }
}

public class EventDelegationDemo {
    public static void main(String[] args) {
        JFrame frame = new JFrame("Event Delegation Demo");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(300, 150);
        frame.setLayout(new FlowLayout());

        // Event Source: JButton
        JButton myButton = new JButton("Click Me");
        frame.add(myButton);

        JLabel statusLabel = new JLabel("Status: Waiting for click...");
        frame.add(statusLabel);

        // 2. Create an Event Listener object
        MyButtonClickListener listener = new MyButtonClickListener(statusLabel);

        // 3. Register the listener with the source
        myButton.addActionListener(listener);

        // Alternative: Using an anonymous inner class for another button
        JButton anotherButton = new JButton("Another Button");
        anotherButton.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                statusLabel.setText("Another Button clicked! Cmd: " + e.getActionCommand());
            }
        });
        frame.add(anotherButton);
        
        // Alternative: Using a lambda expression (Java 8+) for a third button
        JButton lambdaButton = new JButton("Lambda Button");
        lambdaButton.addActionListener(e -> { // e is ActionEvent
            statusLabel.setText("Lambda Button clicked! Source: " + e.getSource().getClass().getSimpleName());
        });
        frame.add(lambdaButton);


        frame.setVisible(true);
    }
}
```

#### 5. Adapter Classes
Adapter classes are convenience classes in the AWT/Swing event handling mechanism. They provide empty (no-op) implementations for all methods in a corresponding listener interface that has more than one method.

*   **Purpose:**
    *   When you are interested in handling only a few events from a multi-method listener interface (like `WindowListener`, `MouseListener`, `KeyListener`), you would normally have to implement all methods of that interface, even if most implementations are empty.
    *   Adapter classes allow you to extend them and override only the methods for the events you care about, making your code cleaner and more concise.

*   **Common Adapter Classes:**
    *   `WindowAdapter` (for `WindowListener`)
    *   `MouseAdapter` (for `MouseListener` and `MouseMotionListener`)
    *   `KeyAdapter` (for `KeyListener`)
    *   `FocusAdapter` (for `FocusListener`)
    *   `ComponentAdapter` (for `ComponentListener`)
    *   `ContainerAdapter` (for `ContainerListener`)

**Example: Using `WindowAdapter` to handle window closing event**

Without `WindowAdapter`, you'd implement `WindowListener`:
```java
/*
import java.awt.event.WindowEvent;
import java.awt.event.WindowListener;
// ...
frame.addWindowListener(new WindowListener() {
    @Override public void windowOpened(WindowEvent e) {}
    @Override public void windowClosing(WindowEvent e) { System.exit(0); } // Only interested in this
    @Override public void windowClosed(WindowEvent e) {}
    @Override public void windowIconified(WindowEvent e) {}
    @Override public void windowDeiconified(WindowEvent e) {}
    @Override public void windowActivated(WindowEvent e) {}
    @Override public void windowDeactivated(WindowEvent e) {}
});
*/
```

With `WindowAdapter`:
```java
import javax.swing.*;
import java.awt.*;
import java.awt.event.WindowAdapter;
import java.awt.event.WindowEvent;

public class AdapterClassDemo {
    public static void main(String[] args) {
        JFrame frame = new JFrame("Adapter Class Demo");
        frame.setSize(300, 200);
        // frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); // This is simpler for just exiting

        // Using WindowAdapter to handle only the windowClosing event
        frame.addWindowListener(new WindowAdapter() {
            @Override
            public void windowClosing(WindowEvent e) {
                System.out.println("Window is closing via WindowAdapter. Exiting application.");
                // Perform any cleanup if necessary
                frame.dispose(); // Release window resources
                System.exit(0);  // Terminate the application
            }

            @Override
            public void windowOpened(WindowEvent e) {
                System.out.println("Window opened!");
            }
            // No need to provide empty implementations for other WindowListener methods
        });

        frame.add(new JLabel("Close this window to see WindowAdapter in action.", SwingConstants.CENTER));
        frame.setVisible(true);
    }
}
```
In this example, by extending `WindowAdapter`, we only need to override `windowClosing()` and optionally `windowOpened()`. The other methods (`windowClosed()`, `windowIconified()`, etc.) have default empty implementations in `WindowAdapter`.

#### 6. JDBC: Strong example program and steps
JDBC (Java Database Connectivity) is a Java API that enables Java applications to connect and interact with databases. It provides methods for querying and updating data in a database.

**Steps for JDBC Operations:**

1.  **Load and Register the JDBC Driver:**
    *   This step loads the specific JDBC driver for the database you are using (e.g., MySQL Connector/J, PostgreSQL JDBC Driver, Oracle JDBC Driver).
    *   Historically, `Class.forName("com.mysql.cj.jdbc.Driver");` was common. With JDBC 4.0 and later, drivers are often automatically registered if they are in the classpath (via SPI - Service Provider Interface). However, explicit loading can still be used.
2.  **Establish a Connection:**
    *   Use `DriverManager.getConnection(url, username, password)` to establish a connection to the database.
    *   The `url` is a string specific to the database driver (e.g., `jdbc:mysql://localhost:3306/mydatabase`).
3.  **Create a Statement:**
    *   Once connected, you need a `Statement` object to send SQL queries to the database.
    *   `Statement stmt = connection.createStatement();` (for simple SQL queries)
    *   `PreparedStatement pstmt = connection.prepareStatement("SQL_QUERY_WITH_PLACEHOLDERS");` (for queries with parameters, offers better performance and security against SQL injection).
    *   `CallableStatement cstmt = connection.prepareCall("{call my_stored_procedure(?,?)}");` (for executing stored procedures).
4.  **Execute the SQL Query:**
    *   For `SELECT` queries (that return data): `ResultSet rs = stmt.executeQuery("SELECT * FROM employees");`
    *   For `INSERT`, `UPDATE`, `DELETE` queries (that modify data and return an update count): `int rowsAffected = stmt.executeUpdate("UPDATE employees SET salary = salary + 5000 WHERE department = 'IT'");`
    *   For DDL statements (`CREATE TABLE`, `DROP TABLE`): `stmt.execute("CREATE TABLE ...");` (returns boolean)
5.  **Process the `ResultSet` (if applicable):**
    *   If the query returns data (a `ResultSet`), iterate through it to retrieve the values.
    *   `while (rs.next()) { ... }` moves the cursor to the next row.
    *   `rs.getInt("column_name")`, `rs.getString("column_label")`, `rs.getDouble(columnIndex)` etc., are used to get data from columns.
6.  **Close the Resources:**
    *   It's crucial to close all JDBC resources (`ResultSet`, `Statement`, `Connection`) in a `finally` block or use try-with-resources (Java 7+) to prevent resource leaks.
    *   Close them in the reverse order of their creation: `ResultSet` -> `Statement` -> `Connection`.

