# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:

Write a program to read a single character from the user without pressing Enter (using System.in.read()).

## AIM:

To write a program to read a single character from the user without pressing Enter (using System.in.read()).

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Inside the main() method, use the statement System.in.read() to read a single character from the keyboard.
4.	Store the returned value (integer ASCII code) in a variable.
5.	Convert the ASCII value to its character equivalent.
6.	Display the character entered by the user.
7.	Display the ASCII value of the character.
8.	End the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103 
*/
```

## SOURCE CODE:
```
import java.io.IOException;

public class ReadSingleChar {
    public static void main(String[] args) throws IOException {
        int ch = System.in.read(); 
        System.out.println("You entered: " + (char) ch);
        System.out.println("ASCII value: " + ch);
    }
}
```
## OUTPUT:

<img width="487" height="291" alt="image" src="https://github.com/user-attachments/assets/f219766b-e40f-46fd-bc2d-6081cbd6db1c" />

## RESULT:

Thus, the java program is implemented successfully and the output is obtained.
