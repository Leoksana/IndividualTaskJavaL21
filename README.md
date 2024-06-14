# IndividualTaskJavaL21
```java
/*develop a simple book management application with Array.List. User should be able to add a book to ArrayList. And to remove a book from ArrayList.*/

import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        List<String> books = new ArrayList<>();         //initialization of ArrayList to store book titles
        Scanner scanner = new Scanner(System.in);         //to read user input
        String userInput;

        System.out.println("Book Management System");
        System.out.println("1. Add a book");
        System.out.println("2. Remove a book");
        System.out.print("Choose an option: ");
        userInput = scanner.nextLine();

        if (userInput.equals("1")) {
            System.out.print("Enter the book title: ");
            String bookTitle = scanner.nextLine();
            books.add(bookTitle);
            System.out.println("\"" + bookTitle + "\" has been added to the list.");
        } else if (userInput.equals("2")) {
            System.out.print("Enter the book title to remove: ");
            String bookToRemove = scanner.nextLine();
            if (books.remove(bookToRemove)) {
                System.out.println("\"" + bookToRemove + "\" has been removed from the list.");
            } else {
                System.out.println("\"" + bookToRemove + "\" not found in the list.");
            }
        } else {
            System.out.println("Invalid option. Please restart the application and choose a valid option.");
        }

        scanner.close();

        System.out.println("\nFinal list of books:");        // Print the final list of books
        for (String book : books) {
            System.out.println("- " + book);
        }

        System.out.println("Exiting the system. Goodbye!");
    }
}
```

```
