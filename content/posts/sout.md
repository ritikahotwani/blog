---
title: "Everything you need to know about Java System.out.println()"
date: 2024-04-05T21:57:15+05:30
description: ""
draft: false
subtitle: ""
header_img: "img/banner.png"
images:
- img/opengraph.png
toc: true
tags: ['Java','OOPs']
categories: []
series: []
comment: true
---

## Introduction
The statement `System.out.println()` is a fundamental piece of code in Java programming, often used for outputting ( printing ) information to the console. 

Let's delve deeper into its meaning and functionality..

## Syntax 
```System.out.println(argument);```

**The argument could be anything**: a number ( integer, float, double ), a word, or a sentence.

## Diving deeper into the meaning

### System :

This is a predefined `final` class in Java's core library (`java.lang package`) that **provides access to system-related properties and methods**.

System is a final class as it cannot be extended. **A class is made final when we need to avoid alteration of base behavior due to the class being extended.**

### out :

This is a `static` member of the `System class`, referring to the standard output stream.

Being **static allows the `out` variable to be accessed directly without the need to create an instance of its class** (in our case the `System class`). This makes it **convenient to access** the standard output stream from anywhere in your code without having to instantiate System.

Like `out`, the system class has other members :

#### in :
`System.in` refers to an **InputStream connected to a standard console to get input**, typically a keyboard. 

Both `System.in`, and `System.out` are **initialized when a Java VM starts by the Java runtime.**

### println() :

This is a method of the `PrintStream class`, which is responsible for printing data to the output stream. 

System class has a `public` and `static` member field called `PrintStream`. 

All instances of the class PrintStream have a `public` method called `println()`.

By declaring it as `public`, it **can be accessed from any other class or package within the Java runtime environment**. This means that any Java code, regardless of its location in the program, can make use of `System.out.println()` for outputting information to the standard output stream.

### Difference between println() and print()
#### println() :

The `println()` method is specifically designed to **print the provided data followed by a newline character**, so each subsequent call to `println()` will print its argument on a new line.

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello");
        System.out.println("world!");
    }
}
```

*output:*

```
Hello
world!
```

#### print() :

The `print()` method is designed **only to print the provided data without adding a newline character**.


```java
public class Main {
    public static void main(String[] args) {
        System.out.print("Hello");
        System.out.print("world!");
    }
}

```

*output:*

```
Helloworld!
```
### Shortcut for System.out.println()

`Static` import of `java.lang.System.out` will **remove the need for the “System.”** part of the statement.

```java
import static java.lang.System.out;

public class Main {
    public static void main(String[] args) {
        out.println("Hello, world!"); // No need for "System." prefix
    }
}

```
**However, the static import isn’t recommended as it decreases code readability.**

#### Keyboard shortcuts

In IDEs like Eclipse, shortcuts like Ctrl+Spacebar can help you be quick while using the statement.

While in VSCode, you can type `sout` and press enter, it will print the statement for you!
