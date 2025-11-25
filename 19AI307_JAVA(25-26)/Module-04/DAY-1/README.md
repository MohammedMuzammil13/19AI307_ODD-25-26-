# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?


## AIM:
To identify and prevent a NullPointerException by ensuring that each array element is not null before calling its toUpperCase() method.


## ALGORITHM :
1. Read a string input from the user.
2. If the input equals "null" (case-insensitive), set str = null; otherwise assign the input to str.
3. Try to convert str to uppercase using toUpperCase().
4. If a NullPointerException occurs, print "Null element".
5. End the program.	





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Mohammed Muzammil A 
RegisterNumber: 212222040103

import java.util.Scanner;

public class NullPointerArrayExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.next();
        String str = input.equalsIgnoreCase("null") ? null : input;

        try {
            System.out.println(str.toUpperCase());
        } catch (NullPointerException e) {
            System.out.println("Null element");
        }

        sc.close();
    }
}

*/
```







## OUTPUT:
<img width="577" height="198" alt="image" src="https://github.com/user-attachments/assets/9db33bc1-350c-4151-ba2c-4987685f81f6" />



## RESULT:
The given program has been executed successfully.
