# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Find the largest digit in a number using wrapper class methods.



## AIM:
To find the largest digit in a number using wrapper class methods.


## ALGORITHM :
1. Read the number as a string.
2. Initialize largest = 0.
3. Loop through each character in the string:
       - Convert the character to a digit.
       - If digit > largest, update largest.
4. After the loop ends, print the value of largest.
5. End the program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Mohammed Muzammil A
RegisterNumber:  212222040103
*/

  
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String numStr = sc.next(); 

        int largest = 0;

        for (int i = 0; i < numStr.length(); i++) {
            int digit = Character.getNumericValue(numStr.charAt(i));

            if (digit > largest)
                largest = digit;
        }

        System.out.println("The largest digit is: " + largest);
    }
}


 

```



## OUTPUT:
<img width="613" height="206" alt="image" src="https://github.com/user-attachments/assets/9382ce64-87ff-4787-8831-84d089b16f6c" />



## RESULT:
The given program has been executed successfully.

