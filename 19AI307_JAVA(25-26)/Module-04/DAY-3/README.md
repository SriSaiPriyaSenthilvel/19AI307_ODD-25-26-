# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:

To demonstrate the Abstract Factory Pattern by creating families of related objects (Herbivore and Carnivore) from two regions — Africa and Asia.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define interfaces for Herbivore and Carnivore.
4.	Create concrete classes for African (Zebra, Lion) and Asian (Deer, Tiger) animals.
5.	Define an AnimalFactory interface with methods to create herbivores and carnivores.
6.	Implement concrete factories: AfricaAnimalFactory and AsiaAnimalFactory.
7.	In main(), use factories to create animals and simulate interactions.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Buffalo implements Herbivore {}
class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Wildebeest(); }
    public Carnivore createCarnivore() { return new Lion(); }
}

class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Buffalo(); }
    public Carnivore createCarnivore() { return new Tiger(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```

## OUTPUT:

<img width="741" height="307" alt="image" src="https://github.com/user-attachments/assets/817f9411-9964-4830-80f6-09b9dc1721db" />

## RESULT:

The program has been executed successfully and the output has been obtained.
