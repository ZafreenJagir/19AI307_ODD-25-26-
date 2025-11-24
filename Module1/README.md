# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS
## QUESTION:
Write a program to print "Hey, my first java program!" using output statement.

### AIM:
To write a Java program that prints the message "Hey, my first java program!" to the screen.

<img width="435" height="149" alt="image" src="https://github.com/user-attachments/assets/6a1477e6-4a4d-4f33-b6a5-cee729d87e39" />

### ALGORITHM :
Start the program.

Define a class named FirstJavaProgram.

Inside the class, define the main() method as the program’s entry point.

Use the statement System.out.println("Hey, my first java program!"); to display the message.

Stop the program.

### PROGRAM:

```
public class FirstJavaProgram {
    public static void main(String[] args) {
        System.out.println("Hey, my first java program!");
    }
}

```

### OUTPUT:

<img width="734" height="180" alt="image" src="https://github.com/user-attachments/assets/a0f4a99d-1a2f-4067-845e-9ada93b58f72" />


### RESULT:
To write a Java program that prints the message "Hey, my first java program!" to the screen.


# Ex.No:1(B) CONDITIONAL STATEMENT
## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.

<img width="222" height="137" alt="image" src="https://github.com/user-attachments/assets/ccd6548e-81a7-47f9-a9bc-4f9b34bb651e" />


### AIM:
To develop a Java program that checks a given floor number and displays a special message based on its divisibility by 3 and/or 5.

### ALGORITHM :
Start the program and read the floor number from the user.

Check if the floor is divisible by both 3 and 5; if true, display "Skipped".

Otherwise, check if the floor is divisible only by 3; if true, display "Beware!".

Otherwise, check if the floor is divisible only by 5; if true, display "Blessings!".

If none of the above conditions are met, display "Floor {floor number}", then stop the program.

### PROGRAM:

```

import java.util.Scanner;

public class MagicalElevator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int floor = scanner.nextInt();

        if (floor % 3 == 0 && floor % 5 == 0) {
            System.out.println("Skipped");
        } else if (floor % 3 == 0) {
            System.out.println("Beware!");
        } else if (floor % 5 == 0) {
            System.out.println("Blessings!");
        } else {
            System.out.println("Floor " + floor);
        }

        scanner.close();
    }
}
```

### OUTPUT:

<img width="457" height="286" alt="image" src="https://github.com/user-attachments/assets/a8cb2c19-3ed1-4aa1-8214-6b8abe48eff3" />


### RESULT:
The program correctly prints “Skipped,” “Beware!,” “Blessings!,” or “Floor {number}” according to the elevator's magical rules.

# Ex.No:1(C) LOOPING STATEMENT
## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

<img width="273" height="132" alt="image" src="https://github.com/user-attachments/assets/56c5a753-06aa-44ce-8131-e81230f06550" />


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

<img width="749" height="256" alt="image" src="https://github.com/user-attachments/assets/f1ece5b8-697e-4d29-afee-c52fb4bc4e46" />


### RESULT:
The program successfully computes and displays the factorial value of the entered number.

# Ex.No:1(D) ARRAYS
## QUESTION:
Write a Java Program to Find the Average of Array Elements.
<img width="464" height="266" alt="image" src="https://github.com/user-attachments/assets/6ffe6583-8481-412c-b65c-f4a8b627ab04" />


### AIM:
To write a Java program that calculates the average of elements in an array.

### ALGORITHM :
Start the program and read the number of elements n from the user.

Create an array of size n and read n integer elements from the user into the array.

Initialize a variable sum to 0 and add all array elements to sum using a loop.

Calculate the average by dividing sum by n and store it in a double variable.

Display the average value and stop the program.

### PROGRAM:

```

import java.util.Scanner;

public class AverageArray {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }
        scanner.close();
        int sum = 0;
        for (int num : arr) {
            sum += num;
        }
        double average = (double) sum / n;
        System.out.printf("The average of elements is %.2f\n", average);
    }
}

```

### OUTPUT:
<img width="794" height="472" alt="image" src="https://github.com/user-attachments/assets/ef3ac82e-c249-4f88-bffe-87640bea9cdc" />



### RESULT:
The program successfully computes and displays the average value of all the array elements entered by the user.

# Ex.No:1(E) STRINGS AND MATH FUNCTION
## QUESTION:
Write a Java program to reverse a given string.

<img width="325" height="118" alt="image" src="https://github.com/user-attachments/assets/6a5375cb-5f2d-4968-9dde-f16bb5bad37f" />


### AIM:
To write a Java program that reverses a given string entered by the user.

### ALGORITHM :
Start the program and read a string input from the user.

Create a StringBuilder object with the input string.

Use the reverse() method of StringBuilder to reverse the string.

Convert the reversed StringBuilder back to a string.

Display the reversed string and stop the program.

### PROGRAM:

```

import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();
        String reversed = new StringBuilder(str).reverse().toString();
        System.out.println("Reversed string: " + reversed);
        scanner.close();
    }
}

```

### OUTPUT:

<img width="729" height="257" alt="image" src="https://github.com/user-attachments/assets/fa0513ce-4d9a-4f4d-9bd1-f875eafbe71a" />


### RESULT:
The program successfully displays the reversed version of the input string.
