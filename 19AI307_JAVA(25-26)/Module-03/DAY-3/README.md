# Ex.No:3(C) ABSTRACTION

## QUESTION:

In a secret intelligence facility, encrypted messages are stored as arrays of characters. Each type of agent has a different way to decode these messages. Define an abstract class Decoder with a method decodeMessage(String[] fragments). There are two types of agents:

AlphaAgent: Extracts a meaningful string by rearranging the fragments based on even indices first, then odd indices, and then reversing the final result.

BetaAgent: Picks all fragments that start and end with the same letter, joins them with -, and removes all vowels from the resulting string.

## AIM:

To create an abstract class Decoder with an abstract method decodeMessage(), and implement two subclasses, AlphaAgent and BetaAgent, each with a unique decoding technique for encrypted message fragments.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class Decoder containing an abstract method decodeMessage(String[] fragments).
4.	Create subclass AlphaAgent implementing decodeMessage() by collecting fragments at even indices,then collecting fragments at odd indices,reversing the combined list.
5.	Joining all fragments into one decoded string.
6.	Create subclass BetaAgent implementing decodeMessage() by selecting fragments whose first and last characters match (case-insensitive).
7.	Joining selected fragments using -.
8.	Removing all vowels from the final combined string.
9.	Read number of fragments and store them in a string array.
10.	Read agent type (1 = AlphaAgent, 2 = BetaAgent).
11.	Create the corresponding agent object.
12.	Call decodeMessage() and print the decoded output.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class Decoder {
    abstract String decodeMessage(String[] fragments);
}


class AlphaAgent extends Decoder {
    @Override
    String decodeMessage(String[] fragments) {
        List<String> ordered = new ArrayList<>();
        
        for (int i = 0; i < fragments.length; i += 2) {
            ordered.add(fragments[i]);
        }
       
        for (int i = 1; i < fragments.length; i += 2) {
            ordered.add(fragments[i]);
        }
       
        Collections.reverse(ordered);
        
        StringBuilder result = new StringBuilder();
        for (String s : ordered) {
            result.append(s);
        }
        return result.toString();
    }
}


class BetaAgent extends Decoder {
    @Override
    String decodeMessage(String[] fragments) {
        List<String> selected = new ArrayList<>();
        for (String f : fragments) {
            if (!f.isEmpty()) {
                char first = Character.toLowerCase(f.charAt(0));
                char last = Character.toLowerCase(f.charAt(f.length() - 1));
                if (first == last) {
                    selected.add(f);
                }
            }
        }

        String joined = String.join("-", selected);
        return joined.replaceAll("[AEIOUaeiou]", "");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine().trim());
        String[] fragments = new String[n];
        for (int i = 0; i < n; i++) {
            fragments[i] = sc.nextLine().trim();
        }
        int type = Integer.parseInt(sc.nextLine().trim());

        Decoder agent;
        if (type == 1)
            agent = new AlphaAgent();
        else
            agent = new BetaAgent();

        System.out.println(agent.decodeMessage(fragments));
        sc.close();
    }
}
```
## OUTPUT:

<img width="628" height="468" alt="image" src="https://github.com/user-attachments/assets/669314fb-4679-47ab-bf95-173022f110bf" />

## RESULT:

The program has been executed successfully and the output has been obtained.
