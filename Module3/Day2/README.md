# Ex.No:3(b) POLYMORPHISM
## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:

area(int side) for square

area(int length, int breadth) for rectangle

area(double radius) for circle


<img width="447" height="180" alt="image" src="https://github.com/user-attachments/assets/8545fae3-180b-43ce-9738-a4f9a6598d34" />


### AIM:
Create an AreaCalculator class using method overloading to calculate areas of a square, rectangle, and circle.

### ALGORITHM :
Start and import Scanner.

Create prog class with overloaded area() methods for square, rectangle, and circle.

Read side, length & breadth, and radius from the user.

Call the appropriate area() method for each shape.

Display the areas and end the program.

### PROGRAM:
``` 
import java.util.Scanner;

class prog {

    void area(int side) {
        System.out.println("Area of square: " + (side * side));
    }

    void area(int length, int breadth) {
        System.out.println("Area of rectangle: " + (length * breadth));
    }

    void area(double radius) {
        double result = Math.PI * radius * radius;
        System.out.println("Area of circle: " + result);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        prog obj = new prog();

        int side = sc.nextInt();
        obj.area(side);

        int length = sc.nextInt();
        int breadth = sc.nextInt();
        obj.area(length, breadth);

        double radius = sc.nextDouble();
        obj.area(radius);

        sc.close();
    }
}
```


### OUTPUT:

<img width="825" height="372" alt="image" src="https://github.com/user-attachments/assets/6757ea20-51a4-4013-b417-b91264ac6d9d" />

### RESULT:
The program displays the area of the chosen shape based on the input values.
