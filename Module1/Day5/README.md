# Ex.No:1(E) STRINGS AND MATH FUNCTION
## QUESTION:
Write a Java program to reverse a given string.

<img width="325" height="118" alt="image" src="https://github.com/user-attachments/assets/f6f19d83-6e0c-4626-b170-996162f00d00" />


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

<img width="729" height="257" alt="image" src="https://github.com/user-attachments/assets/9807c0ff-5145-4f70-9eb9-755969f0d798" />


### RESULT:
The program successfully displays the reversed version of the input string.
