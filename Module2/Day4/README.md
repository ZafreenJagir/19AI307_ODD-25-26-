# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR
## QUESTION:
Write a program to access a static variable using both class name and object.

<img width="398" height="150" alt="image" src="https://github.com/user-attachments/assets/0bc554b1-8bef-4865-b9b7-b3d8d3792731" />



### AIM:
To write a Java program that demonstrates accessing a static variable using both the class name and an object of the class.

### ALGORITHM :
Start the program and declare a static variable num inside the class prog.

In the main() method, read an integer value from the user and assign it to the static variable num.

Access and print the static variable using the class name (prog.num).

Create an object of the class (prog obj = new prog();) and access the static variable using the object (obj.num).

Stop the program after displaying the values.

### PROGRAM:


```

import java.util.Scanner;

class prog {
    
    static int num;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        num = sc.nextInt();
        System.out.println("Accessing using class name: " + prog.num);

        prog obj = new prog();
        System.out.println("Accessing using object: " + obj.num);

        sc.close();
    }
}

```

### OUTPUT:

<img width="797" height="299" alt="image" src="https://github.com/user-attachments/assets/06c7cd43-d5e4-4ffe-afd4-b54c3ec62df4" />


### RESULT:
The program successfully shows that a static variable can be accessed directly via the class name and also through an object, producing the same value.
