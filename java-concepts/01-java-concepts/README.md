# Day 1 — Java Basics & Program Structure

## Overview

This section covers the fundamental structure of a Java program and how Java code is compiled and executed.

The goal of this day is to understand what happens when we write, compile, and run a basic Java application.

---

## Topics Covered

- What is Java?
- JDK, JRE, and JVM
- Structure of a Java program
- Classes
- The `main()` method
- `System.out.print()`
- `System.out.println()`
- `System.out.printf()`
- Comments
- Java compilation and execution
- Command-line arguments

---

## Folder Structure

```text
01-java-basics/
├── HelloWorld.java
├── ProgramStructure.java
├── OutputExample.java
├── Comments.java
├── CommandLineArguments.java
└── README.md

# 1. What is Java?

Java is a high-level, class-based, object-oriented programming language.

It was designed to be portable, meaning Java programs can run on different operating systems when a compatible Java runtime is available.

Java follows the principle:

> Write Once, Run Anywhere

A Java program is written as source code and then compiled into **bytecode**.

The bytecode is executed by the **Java Virtual Machine (JVM)**.

```text
Java Source Code (.java)
        |
        v
Java Compiler (javac)
        |
        v
Bytecode (.class)
        |
        v
Java Virtual Machine (JVM)
        |
        v
Program Execution
```
For example:

```text
HelloWorld.java
      |
      v
    javac
      |
      v
HelloWorld.class
      |
      v
     JVM
      |
      v
Hello, World!

> Note: The exact packaging and terminology have evolved in modern Java versions, but this diagram is a useful conceptual model for understanding the roles of JDK, runtime components, and the JVM.

---

## JDK — Java Development Kit

The **JDK** is used to develop Java applications.

It provides the tools required to:

- Write Java programs
- Compile Java source code
- Run Java applications
- Debug Java programs

One important tool included with the JDK is:

```text
javac
```

The `javac` command is the Java compiler.

Example:

```bash
javac HelloWorld.java
```

The compiler converts:

```text
HelloWorld.java
```

into:

```text
HelloWorld.class
```
The `.class` file contains Java bytecode.

You generally install a JDK when you want to **develop and run Java applications**.

---

## JRE — Java Runtime Environment

The **JRE** represents the runtime environment required to execute Java applications.

Conceptually, it includes:

- JVM
- Java standard libraries
- Runtime components

The JRE provides what is needed to run compiled Java applications.

Conceptually:

The `.class` file contains bytecode.

The JVM loads and executes this bytecode.

The JVM is responsible for several important tasks, including:

- Loading classes
- Verifying bytecode
- Executing bytecode
- Managing memory
- Garbage collection
- Providing runtime services

Execution flow:

```text
Java Source Code
      |
      v
Compiler (javac)
      |
      v
Bytecode (.class)
      |
      v
JVM
      |
      v
Operating System
      |
      v
Program Execution
```

---
## JDK vs JRE vs JVM

| Component | Purpose |
|---|---|
| JDK | Used to develop, compile, and run Java applications |
| JRE | Provides the runtime environment and libraries required to execute Java applications |
| JVM | Executes Java bytecode |

A simple way to remember it:

```text
JDK → Development

JRE → Runtime Environment

JVM → Executes Bytecode
```

Or conceptually:

```text
Developer
    |
    v
   JDK
    |
    v
Compile Java Code
    |
    v
Bytecode
    |
    v
JVM
    |
    v
Program Runs
```

---

## Example

Consider this Java program:

```java
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### Step 1 — Write the Java Source Code

The file is:

```text
HelloWorld.java
```

### Step 2 — Compile the Program

```bash
javac HelloWorld.java
```

This creates:

```text
HelloWorld.class
```

### Step 3 — Run the Program

```bash
java HelloWorld
```

The JVM loads and executes the compiled bytecode.

Output:

```text
Hello, World!
```

---

## Key Takeaways

- Java programs are written in `.java` files.
- Java source code is compiled using `javac`.
- Compilation generates `.class` files.
- `.class` files contain Java bytecode.
- The JVM executes Java bytecode.
- The JDK provides development tools such as the Java compiler.
- The runtime environment provides the libraries and components required to execute Java applications.
- Java's bytecode-and-JVM model enables the same compiled program to run across supported platforms.

---

## Interview Questions

### 1. What is Java?

Java is a high-level, class-based, object-oriented programming language that compiles source code into bytecode, which is executed by the JVM.

### 2. What is the difference between JDK, JRE, and JVM?

- **JDK** provides tools for developing, compiling, and running Java applications.
- **JRE** represents the runtime environment required to execute Java applications.
- **JVM** executes Java bytecode.
