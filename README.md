# oop2
Assignment 1
import java.util.Scanner;
public class Login {
    public static void main(String[] args)
    // Scanner object to read user input
    {
        Scanner scanner = new Scanner(System.in);
        String username = "admin";
        String password = "password";
        int attempts = 0;
      //prompt the user to enter the number of test cases:
        while (attempts < 3) {
            System.out.print("Enter username: ");
            String inputUsername = scanner.nextLine();

            System.out.print("Enter password: ");
            String inputPassword = scanner.nextLine();

            if (inputUsername.equals(username) && inputPassword.equals(password)) {
                System.out.println("Login successful!");
                break;
            } else {
                System.out.println("Incorrect username or password. Please try again.");
                attempts++;
            }
        }

        if (attempts == 3) {
            System.out.println("Too many failed login attempts. Exiting...");
        }
//program closes automatically here
        scanner.close();
    }
}
