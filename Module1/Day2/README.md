# Ex.No:1(B) CONDITIONAL STATEMENT
## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.


<img width="222" height="137" alt="image" src="https://github.com/user-attachments/assets/77e4a577-7618-4830-8881-d4e0cdd6ebc9" />


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


<img width="457" height="286" alt="image" src="https://github.com/user-attachments/assets/3279a599-8d08-4689-bda0-fd402d8f55f9" />


### RESULT:
The program correctly prints “Skipped,” “Beware!,” “Blessings!,” or “Floor {number}” according to the elevator's magical rules.
