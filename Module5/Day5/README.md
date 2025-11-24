# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION
## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

Input:

Two lines: a and b values

Output:

a = <swapped_a>

b = <swapped_b>

### AIM:
To demonstrate the use of a synchronized block for safely swapping two integer variables.

### ALGORITHM :
Read two integer values a and b from the user.
Create a lock object for synchronization.
Use a synchronized(lock) block to perform the swapping.
Swap values using a temporary variable.
Print the swapped values of a and b.
### PROGRAM:
```

import java.util.Scanner;

public class SwapSynchronized {
    private int a;
    private int b;

    public SwapSynchronized(int a, int b) {
        this.a = a;
        this.b = b;
    }

    public void swap() {
        Object lock = new Object(); // lock object for synchronization
        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }
    }

    public void printValues() {
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = Integer.parseInt(sc.nextLine());
        int b = Integer.parseInt(sc.nextLine());

        SwapSynchronized swapper = new SwapSynchronized(a, b);
        swapper.swap();
        swapper.printValues();

        sc.close();
    }
}

```

### OUTPUT:
<img width="1315" height="352" alt="image" src="https://github.com/user-attachments/assets/dad92302-208c-4241-9466-04bbedc2f238" />

### RESULT:
The program successfully swaps the two integers inside a synchronized block and displays the swapped values safely.
