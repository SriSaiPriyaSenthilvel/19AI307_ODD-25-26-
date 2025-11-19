# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

In a magical building, an elevator behaves oddly:
If the floor number is divisible by 3 and 5, it skips that floor.
If the floor number is divisible by 3 only, it says "Beware!".
If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number.

## AIM:

To write a Java program to simulate this elevator logic for a given floor number.

## ALGORITHM :
1.	Start the program.
2. Import the required package java.util.Scanner to read user input.
3.	Create a Scanner object to accept the floor number from the user.
4.	Read the floor number and store it in a variable.
5.	Check if the number is divisible by both 3 and 5:
   If true, display “Skipped”.
6. Else, check if the number is divisible by 3 only:
   If true, display “Beware!”.
7. Else, check if the number is divisible by 5 only:
   If true, display “Blessings!”.
8. Else, if none of the above conditions are satisfied, display the floor number.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String args[]){
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        if(a%3==0 && a%5==0){
            System.out.println("Skipped");
        }
        else if(a%3==0){
            System.out.println("Beware!");
        }
        else if(a%5==0){
            System.out.println("Blessings!");
        }
        else{
            System.out.printf("Floor %d",a);
        }
    }
}
```

## OUTPUT:

<img width="432" height="292" alt="image" src="https://github.com/user-attachments/assets/8a27bebd-7597-4eb9-b119-f7f25955d491" />


## RESULT:

The output for the following java program is executed successfully.
