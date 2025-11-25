# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Read N numbers from user, use a fixed thread pool (size 3) to compute the sum of each number multiplied by 2. Return results in order.

Input:

First line: number of tasks T

Next T lines: integers

 Output:
Each processed result: Result: <n*2>

## AIM:
To use a fixed thread pool (size 3) to compute the sum of each number multiplied by 2. Return results in order.




## ALGORITHM :
1. Read a thread name from the user.
2. Get the current thread using Thread.currentThread().
3. Change the thread’s name to the user-given name.
4. Print the thread’s priority.
5. Print the thread’s updated name.
6. Print the thread object (which includes name, priority, and group).
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Mohammed Muzammil A 
RegisterNumber:  212222040103
*/


import java.util.*;
import java.util.concurrent.*;

public class ThreadPoolDouble {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int T = sc.nextInt();
        List<Integer> nums = new ArrayList<>();
        for (int i = 0; i < T; i++) nums.add(sc.nextInt());

        ExecutorService pool = Executors.newFixedThreadPool(3);
        List<Future<Integer>> results = new ArrayList<>();

        for (int n : nums) {
            results.add(pool.submit(() -> n * 2));
        }

        for (Future<Integer> f : results) {
            System.out.println("Result: " + f.get());
        }

        pool.shutdown();
        sc.close();
    }
}

```







## OUTPUT:
<img width="450" height="383" alt="image" src="https://github.com/user-attachments/assets/1d721917-2f69-4d82-911b-636b3bcee2e2" />




## RESULT:
The given program has been executed successfully.


