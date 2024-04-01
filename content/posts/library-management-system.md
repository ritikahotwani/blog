---
title: " How to create a Library Management System in Java using OOPs"
date: 2024-03-30T20:59:22+05:30
description: ""
draft: false
subtitle: ""
header_img: "img/lib.jpeg"
images:
- default_opengraph.png
toc: true
tags: ['Java','OOPs']
categories: []
series: []
comment: true
---

## Introduction
This blog showcases a simplistic approach to library management system implementation using Object Oriented Programming (OOP).
We will be creating a library management system with the following features : 
1. Add a new book
2. Borrow a book
3. Return a book
4. Display all the books
5. Display available books

The source code of the project : 
[github](https://github.com/ritikahotwani/library-management-system-OOPS)

Link of implementation :
[youtube](https://www.youtube.com/watch?v=EZVrc47gwOs&ab_channel=RitikaHotwani)
## Prerequisites

1. Java JDK installed. [link to install](https://www.oracle.com/in/java/technologies/downloads/)
2. VScode ( or any other IDE of your choice).  [link to install](https://code.visualstudio.com/download)

## Implementation

Start by creating a file named `library.java`.

### Import the libraries

```java
import java.util.HashMap;
import java.util.Scanner;
```

- A **hashmap** is a **data structure** that pairs keys to values. In our case the keys are the book names and the value indicates the availability of the book.
    - 0: indicating book is currently unavailable 
    - 1: book is available.
- The **Scanner class** is used to get user input.

### Create a  Book *class* 

```java
class Book{
    String bookname;
    public Book(String name) {
        bookname= name;
    }  
}
```

The Book class has one attribute `bookname` and a `constructor` ( a special method that is used to initialize objects ).

### Create a *public class* named library ( **should match the name of your file** )

The `public` keyword is used to declare that the class can be accessed by any other class in the same package or from any other package ( here package is the folder where your file is located ).

```java
public class library {
}   
```   

We will be defining the main class and all the methods required for the library management system ( eg. `addBook()`, `borrowBook()`).

#### Initialize the *HashMap*

```java
static HashMap<String, Integer> listOfBooks = new HashMap<String, Integer>();
```

The `static` keyword in Java is used to declare that the members ( variables and methods ) belong to the class rather than to instances of the class. 

Since the list of books stays as it is irrespective of the instances we create, we use the `static` keyword for the `listOfBooks`.

#### Define required methods

1. `addBook()`: Adds a new book to the library
    ```java    
        public static void addBook(String bookname){
            listOfBooks.put(bookname,1);
            System.out.println("Book added!"); 
        }
    ```

    The put method of hashmap adds the book with the book name and value 1.

2. `displayAllBooks()`: Displays all the books
    ```java
        public static void displayAllBooks(){    
            for (String i : listOfBooks.keySet()) {
                System.out.println(i);
            } 
        }
    ``` 

    The for loop iterates over the hashmap keys(bookname) and prints them all.

3. `borrowBook()` : Borrows a book 
    ```java    
    public static void borrowBook(String bookname){
            for (String i : listOfBooks.keySet()) {
                if(i.equals(bookname) && listOfBooks.get(i)==1){
                    System.out.println("You can have the " +bookname + " book. Return after 5 days");
                    listOfBooks.put(i, 0);
                    return;
                }    
            }
            System.out.println("Sorry the book "+bookname+" is out of stock. Come back tomorrow!"); 
        }
    ``` 

    The for loop iterates over the hashmap keys (bookname), finds the book, and checks for its availability.
    If the book is available (1), the book is borrowed and its availability is changed to unavailable (0).

4. `returnBook()`: Returns the borrowed book
    ```java
    public static void returnBook(String bookname) {
            if (listOfBooks.containsKey(bookname)) {
                if (listOfBooks.get(bookname) == 0) {
                    listOfBooks.put(bookname, 1);
                    System.out.println("Thank you for returning the book: " + bookname);
                } 
                else {
                    System.out.println("This book is not currently borrowed.");
                }
            } 
            else {
                System.out.println("Sorry the book " + bookname + " doesn't exist.");
            }
        }
    ```

    The method first checks if the book belongs to the library and its availability.
    Availability is made 1 indicating the book is available back.

5. `displayAvailableBooks()`: displays the available books
    ```java
    public static void displayAvailableBooks(){
        for (String i : listOfBooks.keySet()) {
                if(listOfBooks.get(i)==1){
                    System.out.println(i);
                }    
            }
        }
    ```

    These are the available books i.e. not borrowed by anyone.

#### Define the main class

```java
    public static void main(String[] args) {}
```

In the main class, we will be taking inputs from the user and calling the required methods. 
But before that, declare the scanner class

```java
    Scanner sc = new Scanner(System.in);

```

Now the last and final step:

```java
      while(true){
        System.out.println("Choose your option");
        System.out.println("1.Add a book");
        System.out.println("2.Borrow a book");
        System.out.println("3.Return a book");
        System.out.println("4.Display all books");
        System.out.println("5.Display available books");
        System.out.println("6.exit");
        int option=sc.nextInt();
        sc.nextLine(); // Consume newline character
        switch (option) {
            case 1:
                System.out.println("Book name?");
                String bookname=sc.nextLine();
                if(bookname!=""){
                    addBook(bookname);
                }
                break;
            case 2:
            System.out.println("Book name?");
            String bookToBorrow=sc.nextLine();
                borrowBook(bookToBorrow);
                break;
            case 3:
            System.out.println("Book name?");
            String bookToReturn=sc.nextLine();
                returnBook(bookToReturn);
                break;
            case 4:
                displayAllBooks();
                break;
            case 5:
                displayAvailableBooks();
                break;
            case 6:
                System.out.println("Exiting from library management system!");
                return;

        }
    }
```

The options for performing actions like adding a book, borrowing a book, returning a book, etc are chosen using the Java switch case.
The while loop keeps running until you choose to exit (case 6).

## Conclusion
