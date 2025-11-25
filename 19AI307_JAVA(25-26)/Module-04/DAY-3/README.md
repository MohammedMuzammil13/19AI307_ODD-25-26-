# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
You are asked to simulate a simple Shape Drawing Tool using the Factory Design Pattern in Java.

You will implement a Shape interface with concrete classes for different shapes (Circle, Square, Rectangle). Using a ShapeFactory, your program will take shape names from user input and draw them accordingly. If the shape is unknown, print an error message.

Requirements:
Create a Shape interface with a draw() method.

Implement Circle, Square, and Rectangle classes that implement Shape and override the draw() method to print a specific message.

Implement a ShapeFactory class that returns the correct shape instance based on input.

In your main method, continuously read shape names from the user (using Scanner) until they type "exit" (case-insensitive).

For each valid shape name, create the shape and call draw().

For invalid shapes, print: Invalid shape: <name>


## AIM:
Aim: To implement a Shape Drawing Tool using the Factory Design Pattern in Java, where different shape objects are created and drawn based on user input through a centralized ShapeFactory, ensuring flexible object creation and handling invalid shape requests.


## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read user input.
3. Create a ShapeFactory object.
4. Enter an infinite loop to read shape names repeatedly.
5. Read a shape name from the user and trim extra spaces.
6. If the input equals "exit" (ignoring case), break the loop and stop taking shapes.
7. Use ShapeFactory.getShape() to retrieve the corresponding shape object.
8. If a valid Shape object is returned:
       - Call its draw() method to print the drawing message.
9. If the returned object is null:
       - Print "Invalid shape: <shapeName>".
10. Repeat steps 5–9 until the user types "exit".
11. End the program.






## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Mohammed Muzammil A 
RegisterNumber:  212222040103
*/


import java.util.*;
interface Shape {
    void draw();
}
class Circle implements Shape {
    public void draw() {
        System.out.println("Drawing Circle");
    }
}
class Square implements Shape {
    public void draw() {
        System.out.println("Drawing Square");
    }
}
class Rectangle implements Shape {
    public void draw() {
        System.out.println("Drawing Rectangle");
    }
}
class ShapeFactory {
    public Shape getShape(String shapeType) {
        if (shapeType == null) return null;
        shapeType = shapeType.toLowerCase();
        switch (shapeType) {
            case "circle": return new Circle();
            case "square": return new Square();
            case "rectangle": return new Rectangle();
            default: return null;
        }
    }
}
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ShapeFactory factory = new ShapeFactory();
        while (true) {
            String shapeName = sc.nextLine().trim();
            if (shapeName.equalsIgnoreCase("exit")) break;
            Shape shape = factory.getShape(shapeName);
            if (shape != null) shape.draw();
            else System.out.println("Invalid shape: " + shapeName);
        }
    }
}

```






## OUTPUT:
<img width="672" height="366" alt="image" src="https://github.com/user-attachments/assets/0b7e283f-47ca-4900-a50f-b1e80bdc5acf" />




## RESULT:
The given program has been executed successfully

