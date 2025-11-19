# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

  finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:

To build an inheritance-based Java program that calculates the final price of gold for different types of customers (Regular and Premium), applying respective discounts and showing cashback for premium customers.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Customer with attributes: customerId, name, purchaseWeight, and goldRatePerGram.
4.	Create method getDiscountRate() in base class returning 0 (default).
5.	Create method calculateFinalPrice() that:
calculates discount per gram → discountAmount = goldRatePerGram *      (discountRate/100) and 
 calculates effective rate → effectiveRate = goldRatePerGram - discountAmount
6. Override display() in base class to show general customer details.
7. Create child class RegularCustomer
8. Create child class PremiumCustomer
9. Add calculateCashback() → returns 1% of final price.
10. Override display() to show final price + cashback.
11. Call display() to show the complete bill with discounts.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Sri Sai Priya S
RegisterNumber: 212222240103
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        
    }
}

class RegularCustomer extends Customer {

    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 2.0;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: 2%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
       
    }
}

class PremiumCustomer extends Customer {

    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 5.0;
    }

    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: 5%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
        
    }
}

public class GoldRateSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input 1
        String type1 = sc.next();
        Customer cust1;
        if (type1.equalsIgnoreCase("Regular")) {
            cust1 = new RegularCustomer(sc.next(), sc.next(), sc.nextDouble(), sc.nextDouble());
        } else {
            cust1 = new PremiumCustomer(sc.next(), sc.next(), sc.nextDouble(), sc.nextDouble());
        }

        
        cust1.display();
     

        sc.close();
    }
}
```
## OUTPUT:

<img width="738" height="627" alt="image" src="https://github.com/user-attachments/assets/4771088c-a5bd-45de-9f0c-0df166397e12" />

## RESULT:

The program has been executed successfully and the output has been obtained.

