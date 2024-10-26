# JAVA-Questions

### 1. Given a set command line argument. Find no. of arguments and print the arguments

```java
public class CommandLineArguments {
    public static void main(String[] args) {
        // Print the number of command-line arguments
        System.out.println("Number of command-line arguments: " + args.length);
        
        // Print each command-line argument
        for (int i = 0; i < args.length; i++) {
            System.out.println("Argument " + (i + 1) + ": " + args[i]);
        }
    }
}

```
```sh
java CommandLineArguments hello world how
```
* output
```
Number of command-line arguments: 3
Argument 1: hello
Argument 2: world
Argument 3: how
```

### 2. Enter a number check weather it is odd or even

```java
import java.util.Scanner;

public class OddEvenChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Prompt user to enter a number
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        
        // Check if the number is even or odd
        if (number % 2 == 0) {
            System.out.println(number + " is even.");
        } else {
            System.out.println(number + " is odd.");
        }
        
        scanner.close();
    }
}

```

* output
  
```sh
Enter a number: 5
5 is odd.
```
### 3. Write a program to swap two numbers in java

```java
import java.util.Scanner;

public class SwapNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt user to enter two numbers
        System.out.print("Enter the first number: ");
        int firstNumber = scanner.nextInt();

        System.out.print("Enter the second number: ");
        int secondNumber = scanner.nextInt();

        // Display original values
        System.out.println("\nBefore swap: ");
        System.out.println("First number: " + firstNumber);
        System.out.println("Second number: " + secondNumber);

        // Swap the numbers
        int temp = firstNumber;
        firstNumber = secondNumber;
        secondNumber = temp;

        // Display swapped values
        System.out.println("\nAfter swap: ");
        System.out.println("First number: " + firstNumber);
        System.out.println("Second number: " + secondNumber);

        scanner.close();
    }
}

```

* output

```sh
Enter the first number: 10 
Enter the second number: 20

Before swap:     
First number: 10 
Second number: 20

After swap:      
First number: 20 
Second number: 10
```
