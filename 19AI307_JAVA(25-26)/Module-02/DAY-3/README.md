# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:

To write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create the BankAccount class with private variables and public getter/setter methods.
4.	In main(), create a BankAccount object.
5.	Read the account number and balance from the user.
6.	Set these values using setter methods.
7.	Display the account details using the display() method.
8.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.util.*;
class BankAccount
{
    private String accno;
    private double bal;
    public String getAccountNo()
    {
        return accno;
    }
    public void setAccountNo(String accno)
    { 
        this.accno=accno;
    }
    public double getBalance()
    {
        return bal;
    }
    public void setBalance(double bal)
    {
        this.bal=bal;
    }
    public void display()
    {
        System.out.println("Account Number: "+accno);
        System.out.println("Balance: "+bal);
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        BankAccount o=new BankAccount();
        o.setAccountNo(sc.nextLine());
        o.setBalance(sc.nextDouble());
        o.display();
    }
}
```

## OUTPUT:

<img width="822" height="373" alt="image" src="https://github.com/user-attachments/assets/1a1f476c-9c55-42e4-81bc-fca1973bef5e" />

## RESULT:

Thus, the Java program demonstrating the use of access specifiers with private variables and public getter and setter methods was successfully executed.
