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