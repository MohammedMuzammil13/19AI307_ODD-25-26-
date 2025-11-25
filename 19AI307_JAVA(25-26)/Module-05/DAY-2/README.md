# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents.


## AIM:
To Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using DataOutputStream, and display the byte array contents.


## ALGORITHM :
1. Read an integer n representing the number of strings.
2. Create a ByteArrayOutputStream (baos) to store data in memory.
3. Wrap it with a DataOutputStream (dos) to write UTF strings.
4. Loop n times:
       a. Read a string from user input.
       b. Write the string into dos using writeUTF().
5. Convert the written data into a byte array using baos.toByteArray().
6. Print each byte in the byte array and display the total size.
7. Create a ByteArrayInputStream (bais) using the byte array.
8. Wrap it with a DataInputStream (dis) to read UTF strings back.
9. Loop n times:
       a. Read each string using readUTF().
       b. Print the retrieved string.
10. If any IOException occurs, handle it with an error print.
11. End the program.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Mohammed Muzammil A
RegisterNumber:  2122222040103
*/


import java.io.*;
import java.util.Scanner;

public class UTFStringsInMemoryUserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            DataOutputStream dos = new DataOutputStream(baos);

            int n = scanner.nextInt();
            scanner.nextLine();

            for (int i = 0; i < n; i++) {
                String str = scanner.nextLine();
                dos.writeUTF(str);
            }

            byte[] byteData = baos.toByteArray();

            System.out.println("Byte array contents:");
            for (byte b : byteData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + byteData.length);

            ByteArrayInputStream bais = new ByteArrayInputStream(byteData);
            DataInputStream dis = new DataInputStream(bais);

            System.out.println("\nStrings read from memory:");
            for (int i = 0; i < n; i++) {
                String s = dis.readUTF();
                System.out.println(s);
            }

        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

```





## OUTPUT:
<img width="1022" height="570" alt="image" src="https://github.com/user-attachments/assets/4a890489-9eb1-4ffa-9a93-bc8104972dae" />




## RESULT:
Given program has been executed successfully.

