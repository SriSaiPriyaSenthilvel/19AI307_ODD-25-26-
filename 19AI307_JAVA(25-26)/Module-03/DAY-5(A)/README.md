# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program to define an enum named GameLevel with three constants: EASY, MEDIUM, and HARD.

## AIM:

To write a Java program that defines an enum named GameLevel with constants EASY, MEDIUM, and HARD, and allows the user to select a game level.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define an enum GameLevel with constants: EASY, MEDIUM, HARD.
4.	Read user input as a string and convert it to uppercase.
5.	Use GameLevel.valueOf() to match the input with an enum constant.
6.	If the value matches, print the selected game level.
7.	If no match is found, catch IllegalArgumentException and show an error message.
8.	Close the scanner in the finally block.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

enum GameLevel {
    EASY, MEDIUM, HARD;
}

public class Game {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String userInput = scanner.nextLine().toUpperCase();

        try {
            GameLevel level = GameLevel.valueOf(userInput);
            System.out.println("You selected game level: " + level);
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid game level entered.");
        } finally {
            scanner.close();
        }
    }
}

```

## OUTPUT:

<img width="753" height="185" alt="image" src="https://github.com/user-attachments/assets/fc262597-37bd-4e05-a895-9c609243769d" />

## RESULT:

The program has been executed successfully and the output has been obtained.
