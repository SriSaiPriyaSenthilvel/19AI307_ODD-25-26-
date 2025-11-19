# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.
To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.
Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story):
Only one control tower object should exist.
Every flight contacting it should register its name.
You should log the order of flights that contacted the tower.

Input Format:

First line: Integer n – number of incoming flights
Next n lines: Each line contains the flight name.

Output Format:
For each flight, print:
[FlightName] registered with Radar Control Tower. Total Flights: [count]

## AIM:

To write a java program to simulate this system using the Singleton pattern.

## ALGORITHM :
1.	Start the program and create a Singleton class RadarControlTower with a private       constructor and a static instance.
2.	Provide a getInstance() method to ensure only one tower object is created and         shared.
3.	Maintain a flight counter inside the tower and increment it whenever a flight         registers.
4.	In the main() method, read the number of flights and their names from the user.
5.	For each flight, access the same tower instance, register the flight, and display     the total number of registered flights.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103  
*/
```

## SOURCE CODE:
```
import java.util.*;
class RadarControlTower {
    private static RadarControlTower instance; 
    private int flightCount; 
    private RadarControlTower() {
        flightCount = 0;
    }
    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }
    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine(); 
        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance(); 
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}
```
## OUTPUT:

<img width="1185" height="237" alt="image" src="https://github.com/user-attachments/assets/48b527e3-bbde-4c3b-86ff-e3c264adc79f" />

## RESULT:

Thus, the java program has been implemented successfully and also the output is obtained.

