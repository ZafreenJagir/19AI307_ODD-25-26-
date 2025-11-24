# Ex.No:5(A) INPUTSTREAMREADER
## QUESTION:
Write a Java program to write characters to a file using FileWriter.

### AIM:
To write character data into a file using the FileWriter class in Java.

### ALGORITHM :
Import java.io.FileWriter and java.io.IOException.
Take user input using Scanner.
Create a FileWriter object with the desired file name.
Use write() method to write text into the file.
Close the FileWriter and handle exceptions using try-catch.
### PROGRAM:
```

import java.io.*;

public class FileWriteExample {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            String filename = br.readLine();
            String content = br.readLine();

            FileWriter fw = new FileWriter(filename);
            fw.write(content);
            fw.close();

            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}

```

### OUTPUT:
<img width="1239" height="395" alt="image" src="https://github.com/user-attachments/assets/3e0f7db3-c2ab-43f9-a792-b831939e6de0" />


### RESULT:
The program successfully writes the entered text into output.txt using FileWriter.


# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION
## QUESTION:
Write a Java program to read a string from the user, compress it in memory using ByteArrayOutputStream + GZIPOutputStream, and then decompress it back using ByteArrayInputStream + GZIPInputStream.

### AIM:
To demonstrate string compression and decompression using ByteArrayOutputStream, GZIPOutputStream, ByteArrayInputStream, and GZIPInputStream.

### ALGORITHM :
Read a string from the user.
Create a ByteArrayOutputStream and wrap it in a GZIPOutputStream to compress the string.
Convert the compressed output to a byte array.
Use ByteArrayInputStream and GZIPInputStream to decompress the byte array back to the original string.
Display both compressed size and decompressed string.
### PROGRAM:
```

import java.io.*;
import java.util.Scanner;
import java.util.zip.GZIPOutputStream;
import java.util.zip.GZIPInputStream;

public class GZIPMemoryExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            // Get input string from user
            String input = scanner.nextLine();

            // --- Compress the string ---
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            GZIPOutputStream gzipOut = new GZIPOutputStream(baos);
            gzipOut.write(input.getBytes("UTF-8"));
            gzipOut.close(); // Finish compression

            byte[] compressedData = baos.toByteArray();
            System.out.println("Compressed data (bytes):");
            for (byte b : compressedData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + compressedData.length);

            // --- Decompress the string ---
            ByteArrayInputStream bais = new ByteArrayInputStream(compressedData);
            GZIPInputStream gzipIn = new GZIPInputStream(bais);
            InputStreamReader reader = new InputStreamReader(gzipIn, "UTF-8");
            BufferedReader br = new BufferedReader(reader);

            StringBuilder decompressed = new StringBuilder();
            String line;
            while ((line = br.readLine()) != null) {
                decompressed.append(line);
            }

            System.out.println("\nDecompressed string:");
            System.out.println(decompressed.toString());

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }

        scanner.close();
    }
}

```
### OUTPUT:
<img width="1271" height="577" alt="image" src="https://github.com/user-attachments/assets/6cec78f5-f478-49a2-a308-d23e521c940e" />


### RESULT:
The program successfully compresses and decompresses a string in memory using GZIP streams, showing reduced data size and restoring the original text accurately.


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


# Ex.No:5(D) THREAD PRIORITY
## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

### AIM:
To read a thread name from the user and display the current thread’s name and priority.

### ALGORITHM :
Read the thread name from the user.
Get the reference of the current thread using Thread.currentThread().
Set the name of the current thread using setName().
Retrieve the thread’s name and priority using getName() and getPriority().
Display both values.
### PROGRAM:
```

import java.util.Scanner;

public class ThreadInfoExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Read thread name from user
        String threadName = scanner.nextLine();

        // Create a thread with the given name
        Thread t = new Thread(() -> {
            // Thread work can go here if needed
        }, threadName);

        // Display priority and name
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());

        // Display full thread info (toString())
        System.out.println(t);

        scanner.close();
    }
}
```

### OUTPUT:
<img width="1313" height="265" alt="image" src="https://github.com/user-attachments/assets/0b18b5ca-ea4e-4dd1-9813-097610a45863" />

### RESULT:
The program successfully reads the thread name from the user and displays the current thread’s name and priority.


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

