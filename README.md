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
### 4. Java Program to Find the Sum of Elements in an Array

```java
import java.util.Scanner;

public class ArraySum {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Prompt user to enter the number of elements
        System.out.print("Enter the number of elements in the array: ");
        int n = scanner.nextInt();
        
        // Declare the array and read elements
        int[] array = new int[n];
        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }
        
        // Calculate the sum of elements
        int sum = 0;
        for (int i = 0; i < n; i++) {
            sum += array[i];
        }
        
        // Display the sum
        System.out.println("The sum of the elements in the array is: " + sum);
        
        scanner.close();
    }
}

```

```sh
Enter the number of elements in the array: 5
Enter the elements of the array:
10
20
10
10
10
The sum of the elements in the array is: 60
```
### 5. Java Program to Sort an Array

```java
import java.util.Scanner;

public class BubbleSort {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Prompt user to enter the number of elements
        System.out.print("Enter the number of elements in the array: ");
        int n = scanner.nextInt();
        
        // Declare the array and read elements
        int[] array = new int[n];
        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < n; i++) {
            array[i] = scanner.nextInt();
        }
        
        // Sort the array using Bubble Sort
        for (int i = 0; i < n-1; i++) {
            for (int j = 0; j < n-i-1; j++) {
                if (array[j] > array[j+1]) {
                    // Swap array[j] and array[j+1]
                    int temp = array[j];
                    array[j] = array[j+1];
                    array[j+1] = temp;
                }
            }
        }
        
        // Display the sorted array
        System.out.println("Sorted array:");
        for (int i = 0; i < n; i++) {
            System.out.print(array[i] + " ");
        }
        System.out.println();
        
        scanner.close();
    }
}

```
```sh
Enter the number of elements in the array: 5
Enter the elements of the array:
12
11
5
23
10
Sorted array:
5 10 11 12 23
```
### 6. Add two matrices

```java
import java.util.Scanner;

public class MatrixAddition {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt user to enter the dimensions of the matrices
        System.out.print("Enter the number of rows: ");
        int rows = scanner.nextInt();
        System.out.print("Enter the number of columns: ");
        int columns = scanner.nextInt();

        // Initialize the matrices
        int[][] matrix1 = new int[rows][columns];
        int[][] matrix2 = new int[rows][columns];
        int[][] sumMatrix = new int[rows][columns];

        // Read the elements of the first matrix
        System.out.println("Enter the elements of the first matrix:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                matrix1[i][j] = scanner.nextInt();
            }
        }

        // Read the elements of the second matrix
        System.out.println("Enter the elements of the second matrix:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                matrix2[i][j] = scanner.nextInt();
            }
        }

        // Add the two matrices
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                sumMatrix[i][j] = matrix1[i][j] + matrix2[i][j];
            }
        }

        // Display the sum matrix
        System.out.println("The sum of the two matrices is:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < columns; j++) {
                System.out.print(sumMatrix[i][j] + " ");
            }
            System.out.println();
        }

        scanner.close();
    }
}

```

```sh
Enter the number of rows: 2
Enter the number of columns: 2
Enter the elements of the first matrix:
12
15
14
23
Enter the elements of the second matrix:
10
12
14
13
The sum of the two matrices is:
22 27
28 36
```

### 7. Check a number Palindrome or not

```java
import java.util.Scanner;

public class PalindromeNumberChecker {

    // Function to check if a number is a palindrome
    public static boolean isPalindrome(int number) {
        int originalNumber = number;
        int reversedNumber = 0;

        // Reverse the number using a while loop
        while (number != 0) {
            int digit = number % 10;
            reversedNumber = reversedNumber * 10 + digit;
            number /= 10;
        }

        // Check if the original number is equal to the reversed number
        return originalNumber == reversedNumber;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt user to enter a number
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        // Check if the number is a palindrome
        if (isPalindrome(number)) {
            System.out.println(number + " is a palindrome.");
        } else {
            System.out.println(number + " is not a palindrome.");
        }

        scanner.close();
    }
}


```

```sh
Enter a number: 121
121 is a palindrome.
```
### 8. Implement Method overloading with an example problem

```java
class Addition {

    // Method to add two integers
    public int add(int a, int b) {
        return a + b;
    }

    // Overloaded method to add three integers
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    // Overloaded method to add two doubles
    public double add(double a, double b) {
        return a + b;
    }
}

class MethodOverload {
    public static void main(String[] args) {
        Addition addition = new Addition();

        // Calling overloaded methods
        System.out.println("Sum of 2 and 3 (int): " + addition.add(2, 3));
        System.out.println("Sum of 2, 3 and 4 (int): " + addition.add(2, 3, 4));
        System.out.println("Sum of 2.5 and 3.5 (double): " + addition.add(2.5, 3.5));
    }
}

```
```sh
Sum of 2 and 3 (int): 5
Sum of 2, 3 and 4 (int): 9
Sum of 2.5 and 3.5 (double): 6.0
```
### 9. Using Constructor Find the sum of two numbers

```java
import java.util.Scanner;

class SumOfTwoNumbers {
    private int num1;
    private int num2;
    private int sum;

    // Constructor to initialize the numbers and calculate the sum
    public SumOfTwoNumbers(int num1, int num2) {
        this.num1 = num1;
        this.num2 = num2;
        this.sum = num1 + num2;
    }

    // Method to display the sum
    public void displaySum() {
        System.out.println("The sum of " + num1 + " and " + num2 + " is " + sum);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Prompt user to enter two numbers
        System.out.print("Enter the first number: ");
        int num1 = scanner.nextInt();

        System.out.print("Enter the second number: ");
        int num2 = scanner.nextInt();

        // Create an instance of SumOfTwoNumbers
        SumOfTwoNumbers sumOfTwoNumbers = new SumOfTwoNumbers(num1, num2);

        // Display the sum
        sumOfTwoNumbers.displaySum();

        scanner.close();
    }
}

```

```sh
Enter the first number: 10
Enter the second number: 12
The sum of 10 and 12 is 22
```
### 10. Java Program Demonstrating Method Overriding

```java
// Superclass
class Animal {
    // Method in the superclass
    public void makeSound() {
        System.out.println("The animal makes a sound");
    }
}

// Subclass
class Dog extends Animal {
    // Overriding the makeSound method in the subclass
    @Override
    public void makeSound() {
        System.out.println("The dog barks");
    }
}

class Cat extends Animal {
    // Overriding the makeSound method in the subclass
    @Override
    public void makeSound() {
        System.out.println("The cat meows");
    }
}

// Main Class
public class Overriding {
    public static void main(String[] args) {
        Animal myAnimal = new Animal(); // Create an Animal object
        Animal myDog = new Dog(); // Create a Dog object, but as an Animal reference
        Animal myCat = new Cat();

        // Call the makeSound method on both objects
        myAnimal.makeSound(); // Calls the method from the Animal class
        myDog.makeSound(); // Calls the overridden method from the Dog class
        myCat.makeSound();
    }
}


```

```sh
The animal makes a sound
The dog barks
The cat meows
```
### 11. Java Program Using Inheritance to Find the Area of Different Shapes

```java
// Superclass
abstract class Shape {
    public abstract double calculateArea();
}

// Subclass for Circle
class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}

// Subclass for Rectangle
class Rectangle extends Shape {
    private double length;
    private double width;

    public Rectangle(double length, double width) {
        this.length = length;
        this.width = width;
    }

    @Override
    public double calculateArea() {
        return length * width;
    }
}

// Subclass for Triangle
class Triangle extends Shape {
    private double base;
    private double height;

    public Triangle(double base, double height) {
        this.base = base;
        this.height = height;
    }

    @Override
    public double calculateArea() {
        return 0.5 * base * height;
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {
        Shape circle = new Circle(5);
        Shape rectangle = new Rectangle(4, 6);
        Shape triangle = new Triangle(3, 4);

        System.out.println("Area of the circle: " + circle.calculateArea());
        System.out.println("Area of the rectangle: " + rectangle.calculateArea());
        System.out.println("Area of the triangle: " + triangle.calculateArea());
    }
}

```
```sh
Area of the circle: 78.53981633974483
Area of the rectangle: 24.0
Area of the triangle: 6.0
```
### 12. Java Program Demonstrating an Interface

```java
// Interface
public interface Vehicle {
    void move(); // Abstract method
}

// Class Implementing the Interface - Car
public class Car implements Vehicle {
    @Override
    public void move() {
        System.out.println("The car drives on the road");
    }
}

// Class Implementing the Interface - Bicycle
public class Bicycle implements Vehicle {
    @Override
    public void move() {
        System.out.println("The bicycle rides on the road");
    }
}

// Main Class
public class Main {
    public static void main(String[] args) {
        Vehicle myCar = new Car();
        Vehicle myBicycle = new Bicycle();

        // Calling the move method on both objects
        myCar.move(); // Calls the overridden method in Car
        myBicycle.move(); // Calls the overridden method in Bicycle
    }
}

```
