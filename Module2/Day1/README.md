# Ex.No:2(A) CLASS AND OBJECT
## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

<img width="292" height="173" alt="image" src="https://github.com/user-attachments/assets/62387336-a30f-4d3b-8dcf-de12e0388b2b" />


### AIM:
To create a Java class Car with attributes brand, model, and year, and display the details of two car objects.

### ALGORITHM :
Start the program and define a class Car with attributes brand, model, and year.

Create a constructor in the Car class to initialize the attributes.

Define a display method in the Car class to print the car details with a label.

In the main method, create two Car objects with different attribute values.

Call the display method for each object to print their details and stop the program.

### PROGRAM:
```

class Car {
    String brand;
    String model;
    int year;

    Car(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }

    public void display(String label) {
        System.out.println(label + ": " + brand + " " + model + " " + year);
    }
}

public class CarDemo {
    public static void main(String[] args) {

        Car car1 = new Car("Toyota", "Innova", 2022);
        Car car2 = new Car("Hyundai", "i20", 2021);

        car1.display("Car 1");
        car2.display("Car 2");
    }
}
```

### OUTPUT:
<img width="695" height="186" alt="image" src="https://github.com/user-attachments/assets/7d92ec17-01cf-4d93-8d60-cf0baa9705a4" />


### RESULT:
The program successfully creates two Car objects and prints their brand, model, and year information.
