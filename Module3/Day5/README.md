# Ex.No:3(E) INNER CLASS
## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

### AIM:
To demonstrate accessing an inner class from an outer class in Java.

### ALGORITHM :
Create an outer class with a private variable.
Define an inner class inside it with a method to access the outer variable.
In main(), create an object of the outer class.
Use it to create an object of the inner class.
Call the inner class method.
### PROGRAM:
```

import java.util.Scanner;

class OuterClass {
    String name;

    OuterClass(String name) {
        this.name = name;
    }

    void display() {
        InnerClass inner = new InnerClass();
        inner.showMessage();
    }

    class InnerClass {
        void showMessage() {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("");
        String input = scanner.next();
        scanner.close();

        OuterClass outer = new OuterClass(input);
        outer.display();
    }
}
```

### OUTPUT:

<img width="1223" height="347" alt="image" src="https://github.com/user-attachments/assets/c0efb14d-926a-4be0-9f59-469df61cdff0" />

### RESULT:
The program successfully accesses and prints data from the inner class using the outer class.

# Ex.No:3(F) WRAPPER CLASS
## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

### AIM:
To convert string inputs into integers using the wrapper class and perform addition.

### ALGORITHM :
Read two numbers as strings.
Convert them to integers using Integer.parseInt().
Add the two integers.
Display the sum.
### PROGRAM:

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String str1 = scanner.next();

        String str2 = scanner.next();

        scanner.close();

        try {
            int num1 = Integer.parseInt(str1);
            int num2 = Integer.parseInt(str2);


            int sum = num1 + num2;
            System.out.println("Sum = " + sum);
        } catch (NumberFormatException e) {
            System.out.println("Invalid input. Please enter a valid number.");
        }
    }
}

```

### OUTPUT:
<img width="1223" height="414" alt="image" src="https://github.com/user-attachments/assets/34b5abde-2431-47ee-afd3-703892d5e57c" />


### RESULT:
The program successfully converts strings to integers and displays their sum.

