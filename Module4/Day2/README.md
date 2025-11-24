# Ex.No:4(B) IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM
## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story): Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.

Input Format: First line: Integer n – number of incoming flights

Next n lines: Each line contains the flight name.

Output Format: For each flight, print:

[FlightName] registered with Radar Control Tower. Total Flights: [count]

### AIM:
To simulate a radar control system where only one tower instance handles multiple flight communications using the Singleton pattern.

### ALGORITHM :
Create a RadarControlTower class with a private static instance.
Make the constructor private to prevent multiple object creation.
Define a getInstance() method to return the single instance.
Use a registerFlight() method to log flight names and count.
In main(), get the singleton tower instance and register all flights.
### PROGRAM:
```

import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;
    private int flightCount = 0;

    private RadarControlTower() {}

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();  // consume newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}
```

### OUTPUT:
<img width="1240" height="326" alt="image" src="https://github.com/user-attachments/assets/8eacbb77-16b9-4aae-b8ba-10631fe45043" />

### RESULT:
The program ensures only one Radar Control Tower instance handles all flight communications and correctly displays the total number of registered flights.
