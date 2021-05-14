## Table of Contents
---

- [Hello World](#hello-world)
- [Variables](#variables)
- [DataTypes](#data-types)
- [Change DataTypes](#change-datatypes)
- [If Else](#if-else)
- [For Loop](#for-loops)
- [While Loop](#while-loops)
- [Handle User Input](#handle-user-input)
- [Functions](#functions)
- [Classes](#classes)
- [Try Catch](#try-catch)
- [Lists](#lists)
- [String Operations](#string-operations)
- [List Operations](#list-operations)
- [Null-Safety](https://stackoverflow.com/questions/60068435/what-is-null-safety-in-dart)


## Hello World
---
Basic Hello World program in dart
```dart
    void main() {              // main-function
        print("Hello World");  // Prints "Hello World" in the command line.
    }
```

## Variables
---
A variable is a named space in the memory that stores values. It can contain any type of values for eg String, Integers, Doubles, List etc.

```dart 
    void main() {
        var name = "John";
        var age = 20;
        var interest = 4.5;
        var items = ['Watch', 'Bag', 'Phone'];
    }
```


## Data Types
---
* [Numbers](#numbers)
* [Strings](#strings)
* [Booleans](#booleans)
* [Lists](#lists)
* [Maps](#maps)
* [Dynamic](#dynamic)

    ### Numbers
    \
    Integer - Numerical values with no decimal points.
    ```dart
        void main() {
            int num1 = 10;
            print(num1);
        }
    ```
    Double - Numerical values with decimal points.
    ```dart
        void main() {
            double num1 = 15.5;
            print(num1);
        }
    ```

    ### Strings
    Represents a sequence of characters. These  values are embedded inside 
    double quotes or single quotes.

    ```dart 
        void main() {
            String name = "John";
            String sentence = "This is a sample sentence";
            print(name);
            print(sentence);
        }
    ```

    ### Booleans
    Returns a true or false statement.

    ```dart 
        void main() {
            bool name = true;
            bool age = false;
            print(name); // returns true
            print(age); // returns false
            print(10 > 5); // returns true
        }
    ```

    ### Lists
    It is an ordered group of objects, it can store multiple pieces of informatons at once. It is also reffered to as Arrays in other programming languages.

    ```dart 
        void main() {
            List fruits = ['Apple', 'Orange', 'Grapes', 'Banana'];
            print(fruits);
        }
    ```

    ### Maps
    The Map object is a simple key/value pair. Keys and values in maps can be of any type. It is a dynamic collections.

    ```dart 
        void main() {
            Map users = {'Username': 'John', 'Password': 'John@123'};
            print(users);
        }
    ```

    ### Dynamic
    Using dynamic keyword, you can reassign a variable with different datatype.

    ```dart 
        void main() {
            dynamic age = "Ten";
            print(age);  // prints Ten
            age = 10; // values was reassigned from Ten to 10
            print(age); // prints 10
            age = true; // again reassignes to a boolean
            print(age); // prints true
        }
    ```

## Change DataTypes
---
Change datatypes of any variables in dart.

Convert to Int
```dart
    void main() {
        var age = "10";
        var intAge = int.parse(age); // converts string age to an integer and storing it inside a variable. 
        print(intAge);
    }
```

Convert to a Double
```dart 
    void main() {
        var age = "Ten";
        var doubleAge = int.parse(age).toDouble(); // after parsing it to an integer it converts it into a double.
        print(doubleAge);
    }
```

Convert to a String
```dart
    void main() {
        var age = 25;
        var weight = 70.5;
        var stringAge = age.toString(); // converts int to a string
        var stringWeight = weight.toString();
        print(stringAge);
        print(stringWeight);
    }
```

Convert to a List
```dart 
    void main() {
        var text = "This is a sample text";
        var myList = text.split(' ');
        print(myList);
    }
```
    
## If Else
---
If-else statement are used to implement conditional execution of statements.


### If-Else Statement

```dart 
    if (condition) {
        //return statement
    }
    else {
        // else return statement
    }
```

```dart 
    void main() {
        var age = 20;

        if (age > 18) {
            print("Major");
        }
        else {
            print("Minor");
        }
    }
```

### Else If Statement
It is used to check multiple statements.
```dart 
    if (condition) {
        //return statement
    }
    else if (condition2) {
        //return satement
    }
    else if (condition3) {
        //return statement
    }
    else {
        //else return statement
    }
```

```dart 
    void main() {
        var number = 0;

        if (number > 0) {
            print("Given number is positive");
        }
        else if (number < 0) {
            print("Given number is negative");
        }
        else {
            print("The Given number is 0");
        }
    }
```
## For Loops
---
 A loop represents a set of instructions that must be repeated. In a loop’s context, a repetition is termed as an iteration.

 ```dart
    void main() {
        for(var i = 0; i<10; i++) {  // var i will increase by 1 until it meets the statement in the loop
            print(i);                // numbers from 0 to 9 will be printed
        }
    }
 ```

## While Loops
---
 A while loop is a control flow statement that allows code to be executed repeatedly based on a given Boolean condition. The while loop can be thought of as a repeating if statement.

 ```dart 
    void main() {
        bool chances = true;

        while (chances) {
            print("chances is true");  // This will print continuosly until there is a change in the give condition.
        }
    }
 ```

 ```dart 
    void main() {
        int chances = 0;

        while (chances < 5) {
            print("chance is : ${chances}");  // This will be continuosly printed until the condition chances < 5 becomes false.
            chances++;                        //chances is incremented after each loop.
        }
    }
 ```

 ## Handle User Input
 ---
 This allows the user to give inputs inside the cli.

Get a String userinput
 ```dart 
    import 'dart:io';    // contains input and output functions

    void main() {
        stdout.write("Enter your name : ") // Asks for input
        var name = stdin.readLineSync(); // reads the input from the user and stores it into a variables
        print(name);
    }
 ```

 Reading an Integer input

 ```dart
    import 'dart:io';

    void main() {
        stdout.write('Enter your age: ');
        var age = int.parse(stdin.readLineSync()!); // reads the line and converts it into an int, '!' is for the null check. 
        print(age);
    }
 ```

 ## Functions
 ---
 A function is a block of organized, reusable code that is used to perform a single, related action.

 ```dart 
    void main() {
        add(10, 15); // calling the function below and giving our own parameters.
    }

    void add(int x,y) {  // function to add two integers x and y.
        var result = x + y;
        print(result);
    }
```

## Classes 
---
A class is an extensible program-code-template for creating objects

```dart 
    void main() {
        Operators operators = new Operators();
        operators.addition(10, 15);
        operators.subtraction(25, 20);
        operators.divide(15, 3);
        operators.multiply(25, 4);
}

    class Operators {
        void addition(x, y) {
            print(x + y);
            }

        void subtraction(x, y) {
            print(x - y);
            }

        void divide(x, y) {
            print(x / y);
            }

        void multiply(x, y) {
            print(x * y);
            }
    }
```

## Try Catch
---
```dart 
    void main(){
        var myList = [52, 6, 87];
 
        try {
            for(var i=0;i<10;i++) {
                print(myList[i]);
                }
        } catch (e) {
            print('Something happened while printing the list');
            print('Printing out the message: $e');
    }
    print('Continuing with the rest of the program..');
}
```

## String Operations
---

### Add Strings

```dart 
    void main() {
        String str1 = "Dart";
        String str2 = "Cheat";
        String str3 = "Sheet";
        int num1 = 123;
        print(str1 + str2 + str3 + num1.toString()); // returns DartCheatSheet123
    }
```

### Split Strings

```dart 
    void main() {
        var text = "This is a sample text";
        var myList = text.split(' ');
        print(myList);
    }
```
### Replace Substring in String

```dart
    void main() {
        String para = "This is a sample paragraph";
        String newPara = para.replaceAll("This", "That");
        print(para);
        print(newPara);
    }

```

### Find lenght of a String

```dart 
    void main() {
        String text = "Welcome to Dart";
        print(text.length); // returns the lenght of text.
    }
```

### Trim Strings

```dart 
    void main() {
        String text = "     Welcome to Dart   ";
        print(text); // returns the same text above.
        print(text.trim()); // returns the same string but the unwanted spaces will be removed.
    }
```

## List Operations
---
### Iterate over a list

```dart
    void main() {
        var newList = [10, 15, 40, 25, 70];
        for (int i = 0; i < newList.length; i++) {
            print(newList[i]);
        }
    }
```

### Reverse a List

```dart
    void main() {
        var myList = [10, 15, 40, 25, 30];
        var newList = myList.reversed;
        print(newList);
    }
```

### Add an Element to a List

```dart 
    void main() {
        var myList = [10, 40, 70];
        myList.add(100);
        print(myList);
    }
```

### Remove Element in a List

```dart 
    void main() {
        var myList = [10, 20, 30, 40, 50];
        myList.remove(10); // This will remove 10 from the list.
        myList.removeLast(); // This will remove the last item in the list.
        myList.removeRange(0, 2); // This will remove the values from 10 to 30
    }
```

### Merge two Lists

```dart 
    void main() {
        var list1 = [10, 20, 30, 40, 50];
        var list2 = [60, 70, 80, 90, 100];
        list1.addAll(list2);
        print(list1);
    }
`
