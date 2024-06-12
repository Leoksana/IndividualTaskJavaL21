# IndividualTaskJavaL21
```java
import java.util.ArrayList;
import java.util.Scanner;

public class BookManagementApp {

    private static ArrayList<String> books = new ArrayList<>();

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean exit = false;

        while (!exit) {
            System.out.println("\nBook Management System");
            System.out.println("1. Add a book");
            System.out.println("2. Remove a book");
            System.out.println("3. View all books");
            System.out.println("4. Exit");
            System.out.print("Choose an option: ");

            int choice = scanner.nextInt();
            scanner.nextLine(); // consume the newline

            switch (choice) {
                case 1:
                    addBook(scanner);
                    break;
                case 2:
                    removeBook(scanner);
                    break;
                case 3:
                    viewBooks();
                    break;
                case 4:
                    exit = true;
                    System.out.println("Exiting the application.");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }

        scanner.close();
    }

    private static void addBook(Scanner scanner) {
        System.out.print("Enter the name of the book: ");
        String bookName = scanner.nextLine();
        books.add(bookName);
        System.out.println("Book added successfully.");
    }

    private static void removeBook(Scanner scanner) {
        System.out.print("Enter the name of the book to remove: ");
        String bookName = scanner.nextLine();
        if (books.remove(bookName)) {
            System.out.println("Book removed successfully.");
        } else {
            System.out.println("Book not found.");
        }
    }

    private static void viewBooks() {
        if (books.isEmpty()) {
            System.out.println("No books available.");
        } else {
            System.out.println("Books in the system:");
            for (String book : books) {
                System.out.println("- " + book);
            }
        }
    }
}
```
