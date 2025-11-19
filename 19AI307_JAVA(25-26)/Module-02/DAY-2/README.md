# Ex.No:2(B) METHODS

## QUESTION:

Write a method boolean isEven (int num) without using % operator that returns true if the number is even.

## AIM:

To write a method boolean isEven (int num) without using % operator that returns true if the number is even.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a method isEven(int num) that checks if the number is even by using the logic: A number is even if (num / 2) * 2 is equal to the original number.
4.	In the main() method: Create a Scanner object and read an integer from the user.
5.	Call the isEven() method and display the result.
6.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static boolean isEven(int num)
    {
        return (num/2)*2==num;
    }
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        System.out.println(isEven(num));
    }
}
```

## OUTPUT:

<img width="390" height="183" alt="image" src="https://github.com/user-attachments/assets/090e5fca-35d3-4411-9fe4-12f9020f72e6" />


## RESULT:

Thus, the Java program using a method to check whether a number is even without using the modulo operator (%) was successfully written, executed, and verified.
