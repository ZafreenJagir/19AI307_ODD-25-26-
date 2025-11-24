# Ex.No:1(C) LOOPING STATEMENT
## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.


<img width="273" height="132" alt="image" src="https://github.com/user-attachments/assets/e628be4e-ce5f-43c8-9228-8950b6793409" />


### AIM:
To write a Java program that calculates the factorial of a given number using a for loop.

### ALGORITHM :
Start the program and read an integer n from the user.

Initialize a variable factorial to 1 to store the result.

Use a for loop from 1 to n, multiplying factorial by the loop counter in each iteration.

After the loop ends, print the value of factorial as the factorial of n.

Stop the program.

### PROGRAM:

```

import java.util.Scanner;

public class FactorialCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();  
        long factorial = 1;

        for (int i = 1; i <= n; i++) {
            factorial *= i;
        }

        System.out.println("Factorial of " + n + " is: " + factorial);
    }
}

```

### OUTPUT:

<img width="749" height="256" alt="image" src="https://github.com/user-attachments/assets/59cbb677-9ecc-4991-9938-6676f13b4d4b" />


### RESULT:
The program successfully computes and displays the factorial value of the entered number.
