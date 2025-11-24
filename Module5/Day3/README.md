# Ex.No:5(C) FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.

### AIM:
To count and display the total number of characters in a file using FileReader.

### ALGORITHM :
Ask the user for the file name.
Open the file using FileReader.
Read each character one by one until the end of the file.
Increment a counter for each character read.
Display the total character count.
### PROGRAM:
```

import java.io.*;

public class FileCharacterCount {
    public static void main(String[] args) {
        try {
            // Use BufferedReader to read input
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

            // Read the text to write (assume file name is fixed)
            String text = br.readLine();

            // Use a fixed file name
            String fileName = "output.txt";

            // Write text to file
            try (FileWriter fw = new FileWriter(fileName)) {
                if (text != null) {
                    fw.write(text);
                }
            }

            // Count characters in file
            int charCount = 0;
            try (FileReader fr = new FileReader(fileName)) {
                while (fr.read() != -1) {
                    charCount++;
                }
            }

            System.out.println("Number of characters written to the file: " + charCount);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

### OUTPUT:
<img width="1271" height="303" alt="image" src="https://github.com/user-attachments/assets/d9087cc8-8554-4971-9b59-b51a33fdd64e" />

### RESULT:
The program successfully reads the file and prints the total number of characters present in it.
