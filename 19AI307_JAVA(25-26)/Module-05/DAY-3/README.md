# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## AIM:
To collect a user's name, age, and email through input and store the information in a structured format inside a file named userdata.txt using file handling in Java.


## ALGORITHM :
1. Read the user's name, age, and email from input.
2. Create a FileWriter object for the file "userdata.txt".
3. Write the heading "User Information" and separators into the file.
4. Write the name, age, and email in a structured format.
5. Close the FileWriter.
6. Print the same formatted user information to the console.
7. If any IOException occurs, print an error message.
8. End the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Mohammed Muzammil A 
RegisterNumber:  212222040103
*/


import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read input values
        String name = sc.nextLine();
        String age = sc.nextLine();
        String email = sc.nextLine();

        try {
            FileWriter fw = new FileWriter("userdata.txt");

            fw.write("User Information\n");
            fw.write("================\n");
            fw.write("Name  : " + name + "\n");
            fw.write("Age   : " + age + "\n");
            fw.write("Email : " + email + "\n");

            fw.close();

            // Print output to console exactly as required
            System.out.println("User Information");
            System.out.println("================");
            System.out.println("Name  : " + name);
            System.out.println("Age   : " + age);
            System.out.println("Email : " + email);

        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}

```








## OUTPUT:
<img width="770" height="219" alt="image" src="https://github.com/user-attachments/assets/93dc97d1-3736-4a14-8c50-e254f1d93daa" />




## RESULT:
The given program has been executed successfully.

