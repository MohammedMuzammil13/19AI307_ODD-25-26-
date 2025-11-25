# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User


## AIM:
To write a java program for determine the priority and name of the current thread.



## ALGORITHM :
1. Read a thread name from the user.
2. Get the current thread using Thread.currentThread().
3. Set the thread’s name to the user-provided name.
4. Print the thread’s priority.
5. Print the thread’s updated name.
6. Print the thread object itself (which shows name and priority).
7. End the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Mohammed Muzammil A
RegisterNumber:  212222040103
*/


import java.util.Scanner;

public class ThreadInfo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String threadName = sc.nextLine();

        Thread t = Thread.currentThread();
        t.setName(threadName);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
        
        sc.close();
    }
}

```



## OUTPUT:
<img width="699" height="173" alt="image" src="https://github.com/user-attachments/assets/df4b7197-be9c-4871-b86a-f6cfde0cf148" />




## RESULT:
The given program has been executed successfully.

