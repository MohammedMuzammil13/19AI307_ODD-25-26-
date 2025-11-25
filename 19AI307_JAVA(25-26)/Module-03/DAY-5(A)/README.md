# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to define an enum named Department with constants like CS, IT, and ECE. Each constant should hold a full form string like "Computer Science" using a constructor.


## AIM:
To write a Java program to define an enum named Department with constants like CS, IT, and ECE. Each constant should hold a full form string like "Computer Science" using a constructor.


## ALGORITHM :
1. Read the department code as input.
2. Convert the input to uppercase.
3. Try to get the corresponding enum constant using Department.valueOf().
4. If found, print its full form using getFullForm().
5. If an exception occurs, print "Invalid department code entered."





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Mohammed Muzammil A
RegisterNumber: 212222040103
*/


   
import java.util.*;

enum Department {
    CS("Computer Science"),
    IT("Information Technology"),
    ECE("Electronics and Communication Engineering");

    private String fullForm;

    Department(String fullForm) {
        this.fullForm = fullForm;
    }

    public String getFullForm() {
        return fullForm;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.next().toUpperCase();

        try {
            Department dept = Department.valueOf(input);
            System.out.println("Full Form: " + dept.getFullForm());
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid department code entered.");
        }
    }
}



```








## OUTPUT:
<img width="1060" height="244" alt="image" src="https://github.com/user-attachments/assets/3496f365-d2a5-4c90-965b-1524ff22ec40" />




## RESULT:
The given program has been executed successfully.

