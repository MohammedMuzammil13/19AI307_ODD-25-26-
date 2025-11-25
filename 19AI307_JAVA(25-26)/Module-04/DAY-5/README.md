# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed. (Mediator Pattern)

## AIM:
To create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed. 


## ALGORITHM :
1. Start the program.
2. Create a ChatRoom object.
3. Read two usernames from input and create two User objects, automatically registering them in the ChatRoom.
4. Read an integer n representing the number of messages to process.
5. Loop n times:
       a. Read the sender's name.
       b. Read the receiver's name.
       c. Read the message text.
       d. If the sender matches user1, call user1.send(receiver, message).
       e. Else if the sender matches user2, call user2.send(receiver, message).
       f. Otherwise print "Unknown sender".
6. Inside send(), the ChatRoom sends the message to the receiver.
7. If the receiver exists, print "<from> to <to>: <message>".
8. If the receiver does not exist, print "User <name> not found".
9. End the program.






## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: 212222040103
RegisterNumber:  Mohammed Muzammil A
*/


import java.util.*;

class ChatRoom {
    private Map<String, User> users = new HashMap<>();

    public void registerUser(User user) {
        users.put(user.getName(), user);
    }

    public void sendMessage(String from, String to, String message) {
        User receiver = users.get(to);
        if (receiver != null) {
            receiver.receive(from, message);
        } else {
            System.out.println("User " + to + " not found");
        }
    }
}

class User {
    private String name;
    private ChatRoom chatRoom;

    public User(String name, ChatRoom chatRoom) {
        this.name = name;
        this.chatRoom = chatRoom;
        chatRoom.registerUser(this);
    }

    public String getName() {
        return name;
    }

    public void send(String to, String message) {
        chatRoom.sendMessage(name, to, message);
    }

    public void receive(String from, String message) {
        System.out.println(from + " to " + name + ": " + message);
    }
}

public class ChatApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        ChatRoom room = new ChatRoom();
        User user1 = new User(sc.nextLine(), room); // e.g., Alice
        User user2 = new User(sc.nextLine(), room); // e.g., Bob

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String sender = sc.nextLine();
            String receiver = sc.nextLine();
            String message = sc.nextLine();

            if (sender.equals(user1.getName())) {
                user1.send(receiver, message);
            } else if (sender.equals(user2.getName())) {
                user2.send(receiver, message);
            } else {
                System.out.println("Unknown sender");
            }
        }

        sc.close();
    }
}

```






## OUTPUT:
<img width="972" height="600" alt="image" src="https://github.com/user-attachments/assets/0a6a18fd-c541-4baa-ab5a-85f3f61d3283" />




## RESULT:
The given program has been successfully executed.

