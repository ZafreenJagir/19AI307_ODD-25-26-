# Ex.No:2(B) METHODS
## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.

When staticMethod() is called, it should print "I am static".

When nonStaticMethod() is called, it should print "I am non-static"

<img width="169" height="153" alt="image" src="https://github.com/user-attachments/assets/50295d5f-cf36-431a-9cbf-fe1f3960c7d7" />


### AIM:
To create a Java class with one static method and one non-static method, and demonstrate calling both from the main() method.

### ALGORITHM :
Start the program and define a class MyClass.

Create a static method staticMethod() that prints "I am static".

Create a non-static method nonStaticMethod() that prints "I am non-static".

In the main() method, call the static method directly using the class name.

Create an object of MyClass and call the non-static method using this object, then stop the program.

### PROGRAM:

```

public class MyClass {
    public static void staticMethod() {
        System.out.println("I am static");
    }
    public void nonStaticMethod() {
        System.out.println("I am non-static");
    }

    public static void main(String[] args) {
        MyClass.staticMethod();
        MyClass obj = new MyClass();
        obj.nonStaticMethod();
    }
}

```

### OUTPUT:

<img width="415" height="177" alt="image" src="https://github.com/user-attachments/assets/df58c915-5ca9-4389-b516-bcf2e60ffdac" />


### RESULT:
The program successfully calls the static method to print “I am static” and the non-static method to print “I am non-static”.
