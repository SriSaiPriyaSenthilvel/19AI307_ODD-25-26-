# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to check if a number is prime using wrapper classes.

## AIM:

To write a Java program that checks whether a given number is prime by using the Integer wrapper class for parsing and handling the input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read input from the user as a string.
4.	Use the Integer.parseInt() method (wrapper class) to convert the input into an integer.
5.	If parsing fails, catch NumberFormatException and display an error message.
6.	If the number is less than or equal to 1, it is not prime.
7.	If any divisor divides the number completely, mark it as not prime.
8.	After checking, print whether the number is prime or not.
9.	Close the scanner.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class PrimeChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        
        String input = scanner.nextLine();

        try {
            Integer number = Integer.parseInt(input); // Using Integer wrapper class

            if (number <= 1) {
                System.out.println(number + " is not a prime number.");
            } else {
                boolean isPrime = true;
                for (int i = 2; i <= Math.sqrt(number); i++) {
                    if (number % i == 0) {
                        isPrime = false;
                        break;
                    }
                }

                if (isPrime) {
                    System.out.println(number + " is a prime number.");
                } else {
                    System.out.println(number + " is not a prime number.");
                }
            }

        } catch (NumberFormatException e) {
            System.out.println("Invalid input. Please enter a valid integer.");
        }

        scanner.close();
    }
}
```

## OUTPUT:

<img width="608" height="210" alt="image" src="https://github.com/user-attachments/assets/40870e28-64f3-4eb1-9915-dbe33bacd771" />

## RESULT:

The program has been executed successfully and the output has been obtained.
