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
Argument 1: arg1
Argument 2: arg2
Argument 3: arg3
```
