# Ex.No:2(E) ACCESS MODIFIERS
## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

import java.util.Scanner;

class Calculator { // Your Methods here }

class prog { public static void main(String[] args) { // Your Function Initiation here } }

<img width="366" height="184" alt="image" src="https://github.com/user-attachments/assets/eedb0ea8-e601-4efe-80e6-71678fde71dd" />


### AIM:
Create a Calculator class with a non-static add() method to sum two numbers and a static info() method to display a message.

### ALGORITHM :
Start and import Scanner to read input.

Define Calculator class with a non-static add(a, b) method and a static info() method.

Read two integers from the user using Scanner.

Call Calculator.info() and use a Calculator object to calculate the sum with add(a, b).

Display the sum and end the program.

### PROGRAM:

```

import java.util.Scanner;

class Calculator {
    
    public int add(int a, int b) {
        return a + b;
    }

    public static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        Calculator.info();

        Calculator calc = new Calculator();
        int sum = calc.add(a, b);

        System.out.println("Sum: " + sum);

        sc.close();
    }
}

```

### OUTPUT:

<img width="576" height="291" alt="image" src="https://github.com/user-attachments/assets/7882e50a-bf71-4bfb-9f46-bc0ee1d6ccdf" />


### RESULT:
The program displays "Calculator is ready", takes two numbers as input, and then shows their sum.
