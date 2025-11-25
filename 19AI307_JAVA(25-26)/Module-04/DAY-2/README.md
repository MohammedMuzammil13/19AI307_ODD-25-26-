# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.

The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.

Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

Hidden Clue:
Use Singleton to manage shared access.

Count and log each print job submission.

Validate that state is preserved across all accesses.

## AIM:
To implement a Singleton-based Print Spooler Manager that ensures only one shared instance handles all print job submissions while maintaining a consistent job count across multiple accesses.


## ALGORITHM :
1. Start the program.
2. Read an integer n representing the number of print job submissions.
3. Loop from 1 to n:
       a. Read the department name as input.
       b. Access the singleton instance using PrintSpoolerManager.getInstance().
       c. Submit a print job through submitJob(department).
       d. Receive the updated job count.
       e. Print the department name and the total jobs in the queue.
4. Continue until all n submissions are processed.
5. End the program.






## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Mohammed Muzammil A
RegisterNumber:  212222040103
*/


import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance = null;
    private int jobCount;

    private PrintSpoolerManager() {
        jobCount = 0;
    }

    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public int submitJob(String department) {
        jobCount++;
        return jobCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}

```





## OUTPUT:
<img width="1181" height="356" alt="image" src="https://github.com/user-attachments/assets/4febd09b-f780-456b-ad41-ff554044db88" />



## RESULT:
The given program has been executed successfully.

