# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:

To write a Java program that calculates the factorial of a given number using a looping statement.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number n from the user.
4.	Initialize fact = 1.
5.	Use a for loop from 1 to n and multiply each value with fact.
6.	Display the final factorial value.
7.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[]args)
    {
        Scanner in=new Scanner(System.in);
        int num=in.nextInt();
        int fact = 1;
        for(int i=1;i<=num;i++)
        {
            fact=fact*i;
        }
        System.out.println("Factorial of "+num+" is: "+fact);
    }
}
```

## OUTPUT:

<img width="792" height="270" alt="image" src="https://github.com/user-attachments/assets/8825b0bb-431e-4faa-a257-b7d7b88e1a18" />

## RESULT:

Thus, the program to calculate the factorial of a number using a for loop was successfully executed.

