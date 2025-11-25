# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You need to clone documents. Implement the Prototype Pattern to copy a Document object with a title and content. On user input, create a copy and print both the original and the clone.


## AIM:
To implement the Prototype Pattern to copy a Document object with a title and content. On user input, create a copy and print both the original and the clone.

## ALGORITHM :
1. Read the document title from the user.
2. Read the document content from the user.
3. Create an original Document object using the provided title and content.
4. Clone the original document using the clone() method.
5. Display the original document with the label "Original".
6. Display the cloned document with the label "Cloned".
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Mohammed Muzammil A 
RegisterNumber:  212222040103
*/


import java.util.Scanner;

class Document implements Cloneable {
    String title, content;
    public Document(String title, String content) {
        this.title = title;
        this.content = content;
    }
    public Document clone() {
        try {
            return (Document) super.clone();
        } catch (CloneNotSupportedException e) {
            return null;
        }
    }
    public void display(String label) {
        System.out.println(label + ": " + title + " - " + content);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String title = scanner.nextLine();
        String content = scanner.nextLine();
        Document original = new Document(title, content);
        Document clone = original.clone();
        original.display("Original");
        clone.display("Cloned");
    }
}

```





## OUTPUT:
<img width="1105" height="255" alt="image" src="https://github.com/user-attachments/assets/ca13b10c-c39d-4f5d-ac96-d9f5cbb10cf3" />




## RESULT:
The given program has been executed successfully

