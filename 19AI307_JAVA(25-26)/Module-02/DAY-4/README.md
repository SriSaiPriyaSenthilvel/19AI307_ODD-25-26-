# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a java program using class to perform addition of two numbers using parameterised constructor.

## AIM:

To write a java program using class to perform addition of two numbers using parameterised constructor.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Addition with two variables and a parameterised constructor.
4.	In the constructor, add the two numbers and print the result.
5.	In main(), read two numbers from the user.
6.	Create an object of Addition and pass the numbers to the constructor.
7.	End the program

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103 
*/
```

## SOURCE CODE:
```
import java.util.*;
class Addition
{
    int n1,n2;
    Addition(int n1, int n2)
    {
        int sum=n1+n2;
        System.out.println("Sum = "+sum);
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n1=sc.nextInt();
        int n2=sc.nextInt();
        Addition o=new Addition(n1,n2);
    }
}
```

## OUTPUT:

<img width="419" height="309" alt="image" src="https://github.com/user-attachments/assets/85a99b84-5bed-430f-8ab1-653463819c25" />


## RESULT:

Thus, a Java program to perform addition of two numbers using a parameterised constructor was successfully written and executed.

