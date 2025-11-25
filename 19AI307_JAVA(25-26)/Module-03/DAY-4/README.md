# Ex.No:3(D)    INTERFACE 

## QUESTION:
In the land of Eldoria, two kinds of advisors (Strategic and Emergency) suggest how much resources to allocate based on the kingdom’s stress factors.

StrategicAdvisor: Advises cautiously in normal times.

EmergencyAdvisor: Takes aggressive decisions during crisis.

Define an abstract class Advisor with a method adviseLevel() that returns "Minimal", "Balanced", or "Critical" depending on the internal logic.

Requirements:

Strategic Advisor:

If unrestLevel < 3 → Minimal

unrestLevel 3–6 → Balanced

unrestLevel ≥ 7 → Critical

Emergency Advisor:

If dangerLevel + disasterCount ≥ 15 → Critical

If dangerLevel ≥ 7 → Balanced

Otherwise → Minimal

Input Format:

Line 1: Advisor type  
Line 2: unrestLevel (type 1) OR dangerLevel disasterCount (type 2)

Output Format:

"Minimal" / "Balanced" / "Critical"


## AIM:
To determine the advisor’s resource allocation level based on given conditions using an abstract class and subclass-specific logic.


## ALGORITHM :
1. Input advisor type.
2. Input required values based on the type.
3. Create the corresponding advisor object.
4. Call its adviseLevel() method.
5. Print the returned advice level.






## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Mohammed Muzammil A
RegisterNumber:  212222040103
*/

   

import java.util.*;

abstract class Advisor {
    abstract String adviseLevel();
}

class StrategicAdvisor extends Advisor {
    int unrestLevel;

    StrategicAdvisor(int unrestLevel) {
        this.unrestLevel = unrestLevel;
    }

    String adviseLevel() {
        if (unrestLevel < 3) return "Minimal";
        else if (unrestLevel <= 6) return "Balanced";
        else return "Critical";
    }
}

class EmergencyAdvisor extends Advisor {
    int dangerLevel, disasterCount;

    EmergencyAdvisor(int dangerLevel, int disasterCount) {
        this.dangerLevel = dangerLevel;
        this.disasterCount = disasterCount;
    }

    String adviseLevel() {
        if (dangerLevel + disasterCount >= 15) return "Critical";
        else if (dangerLevel >= 7) return "Balanced";
        else return "Minimal";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();

        Advisor advisor;
        if (type == 1) {
            int unrestLevel = sc.nextInt();
            advisor = new StrategicAdvisor(unrestLevel);
        } else {
            int dangerLevel = sc.nextInt();
            int disasterCount = sc.nextInt();
            advisor = new EmergencyAdvisor(dangerLevel, disasterCount);
        }

        System.out.println(advisor.adviseLevel());
        sc.close();
    }
}



```








## OUTPUT:
<img width="495" height="222" alt="image" src="https://github.com/user-attachments/assets/50bf7441-f261-4afe-b67c-c1fa72fbf7de" />



## RESULT:
The given program has been executed and verified successfully.

