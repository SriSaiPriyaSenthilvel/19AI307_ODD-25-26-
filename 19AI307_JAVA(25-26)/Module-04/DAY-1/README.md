# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

Write a program that reads an integer from the user. The program must reject any negative number by throwing a special error. Design a custom exception to handle this and message to display if the user enters a negative number.

## AIM:

To write a program that reads an integer from the user. The program must reject any negative number by throwing a special error. Design a custom exception to handle this and message to display if the user enters a negative number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class NegativeNumberException extends Exception {
    public NegativeNumberException(String message) {
        super(message);
    }
}
public class CustomExceptionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        sc.close();
        try {
            if (num < 0) {
                throw new NegativeNumberException("Negative numbers are not allowed");
            }
            System.out.println("Valid input: " + num);
            
        } catch (NegativeNumberException e) {
            System.out.println(e.getMessage());
        }
    }
}
```
## OUTPUT:

<img width="826" height="275" alt="image" src="https://github.com/user-attachments/assets/442a8c52-aba8-4f64-a866-084ba8828ad6" />

## RESULT:

Thus, the Java program demonstrating the use of exception handling was successfully executed.
