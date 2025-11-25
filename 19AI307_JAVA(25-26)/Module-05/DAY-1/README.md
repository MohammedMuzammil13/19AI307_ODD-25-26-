# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to create a new file and write user-provided content into it.

## AIM:
To write a Java program to create a new file and write user-provided content into it.


## ALGORITHM :
1. Read the file name from the user.
2. Read the content to be written into the file.
3. Create a File object using the given file name.
4. Attempt to create the file using createNewFile():
       - If the file is newly created, print a creation message.
       - If the file already exists, print a message indicating existing file.
5. Create a FileWriter object for the file.
6. Write the user-provided content into the file.
7. Close the FileWriter.
8. Print a message confirming successful writing.
9. If any IOException occurs, print an error message.
10. End the program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Mohammed Muzammil A
RegisterNumber:  212222040103
*/

import java.io.*;
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String fileName = sc.nextLine();

        String content = sc.nextLine();

        try {
    
            File file = new File(fileName);

            if (file.createNewFile()) {
                System.out.println("File created: " + fileName);
            } else {
                System.out.println("File already exists. Writing content...");
            }

            FileWriter writer = new FileWriter(file);
            writer.write(content);
            writer.close();

            System.out.println("Content written to the file successfully.");

        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }
}

```







## OUTPUT:
<img width="976" height="258" alt="image" src="https://github.com/user-attachments/assets/f8a633b1-9f82-4039-8d11-b47aef20a938" />




## RESULT:
The given program has been executed successfully.
