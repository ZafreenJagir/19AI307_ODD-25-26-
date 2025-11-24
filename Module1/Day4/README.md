# Ex.No:1(D) ARRAYS
## QUESTION:
Write a Java Program to Find the Average of Array Elements.

<img width="464" height="266" alt="image" src="https://github.com/user-attachments/assets/bee58b43-52ea-4397-9cde-4c3e38ae4e4a" />


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

<img width="794" height="472" alt="image" src="https://github.com/user-attachments/assets/1f3a042d-2bfc-45c4-8d92-2273b779dbcb" />


### RESULT:

The program successfully computes and displays the average value of all the array elements entered by the user.
