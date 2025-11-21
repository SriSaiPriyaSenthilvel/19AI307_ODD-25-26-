# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

Write a program to count the number of characters in a file.

## AIM:

To count and display the total number of characters in a file using FileReader.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Ask the user for the file name.
4.	Open the file using FileReader.
5.	Read each character one by one until the end of the file.
6.	Increment a counter for each character read.
7.	Display the total character count.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.io.*;

public class FileCharacterCount {
    public static void main(String[] args) {
        try {
            // Use BufferedReader to read input
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

            // Read the text to write (assume file name is fixed)
            String text = br.readLine();

            // Use a fixed file name
            String fileName = "output.txt";

            // Write text to file
            try (FileWriter fw = new FileWriter(fileName)) {
                if (text != null) {
                    fw.write(text);
                }
            }

            // Count characters in file
            int charCount = 0;
            try (FileReader fr = new FileReader(fileName)) {
                while (fr.read() != -1) {
                    charCount++;
                }
            }

            System.out.println("Number of characters written to the file: " + charCount);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

## OUTPUT:

<img width="847" height="182" alt="image" src="https://github.com/user-attachments/assets/b4fff857-39c4-4de3-b2d3-d7bb29cf4f64" />

## RESULT:

The program successfully reads the file and prints the total number of characters present in it.
