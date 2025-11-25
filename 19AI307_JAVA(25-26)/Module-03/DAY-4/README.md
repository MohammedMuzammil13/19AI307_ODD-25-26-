# Ex.No:3(D)    INTERFACE 

## QUESTION:
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.


AggressiveController: Allows only if "GREEN".

DefensiveController: Allows for "GREEN" or "YELLOW".

 Input Format:

signalColor
controllerType
signalColor: A string indicating the signal color (GREEN, YELLOW, RED)

controllerType: An integer (1 for AggressiveController, 2 for DefensiveController)

 Output Format:

Print "GO"       → if vehicle is allowed to move  
Print "STOP"     → if vehicle must stop


## AIM:
To implement a program that decides vehicle movement by using two controller classes with different signal-handling logic, and output whether the vehicle should "GO" or "STOP" based on the input signal color and controller type.


## ALGORITHM :
1. Read the signal color and controller type from input.
2. If controller type is 1, create an AggressiveController object.
   Else create a DefensiveController object.
3. Call canGo(signalColor) on the selected controller.
4. If the method returns true, print "GO".
5. Otherwise, print "STOP".





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Mohammed Muzammil A
RegisterNumber:  212222040103
*/


   
import java.util.*;

interface TrafficController {
    boolean canGo(String signalColor);
}

class AggressiveController implements TrafficController {
    public boolean canGo(String signalColor) {
        return signalColor.equalsIgnoreCase("GREEN");
    }
}

class DefensiveController implements TrafficController {
    public boolean canGo(String signalColor) {
        return signalColor.equalsIgnoreCase("GREEN") || signalColor.equalsIgnoreCase("YELLOW");
    }
}

public class TrafficControlSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String signalColor = sc.next().trim().toUpperCase();
        int controllerType = sc.nextInt();
        TrafficController controller;

        if (controllerType == 1) {
            controller = new AggressiveController();
        } else if (controllerType == 2) {
            controller = new DefensiveController();
        } else {
            System.out.println("STOP");
            sc.close();
            return;
        }

        if (controller.canGo(signalColor)) {
            System.out.println("GO");
        } else {
            System.out.println("STOP");
        }

    }
}




```








## OUTPUT:
<img width="369" height="181" alt="image" src="https://github.com/user-attachments/assets/f22f582f-ce59-4440-ad15-b140fdf4e78a" />




## RESULT:
The given program has been executed successfully.

