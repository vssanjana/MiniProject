import java.util.Scanner;
import java.util.Random;

public class Email {
    private String firstName;
    private String lastName;
    private String password;
    private String department;
    private int mailboxCapacity = 500;
    private String alternateEmail;
    private String companySuffix = "company.com";
    private String email;
    
    // Constructor to receive first name and last name
    public Email(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
        
        // Call method to ask for department
        this.department = setDepartment();
        
        // Generate email address
        this.email = firstName.toLowerCase() + "." + lastName.toLowerCase() + "@" + department + "." + companySuffix;
        
        // Generate a random password
        this.password = generatePassword(8);
        System.out.println("Your generated password is: " + this.password);
    }

    // Ask for department
    private String setDepartment() {
        System.out.println("Enter department:\n1. Sales\n2. Development\n3. Accounting\n0. None");
        Scanner scanner = new Scanner(System.in);
        int choice = scanner.nextInt();
        switch (choice) {
            case 1: return "sales";
            case 2: return "dev";
            case 3: return "acct";
            default: return "general";
        }
    }

    // Generate a random password
    private String generatePassword(int length) {
        String passwordSet = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%";
        Random random = new Random();
        char[] password = new char[length];
        for (int i = 0; i < length; i++) {
            password[i] = passwordSet.charAt(random.nextInt(passwordSet.length()));
        }
        return new String(password);
    }

    // Set mailbox capacity
    public void setMailboxCapacity(int capacity) {
        this.mailboxCapacity = capacity;
    }

    // Set alternate email
    public void setAlternateEmail(String altEmail) {
        this.alternateEmail = altEmail;
    }

    // Change password
    public void changePassword(String password) {
        this.password = password;
    }

    // Display user info
    public String showInfo() {
        return "NAME: " + firstName + " " + lastName +
               "\nEMAIL: " + email +
               "\nMAILBOX CAPACITY: " + mailboxCapacity + "mb";
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Get user input for first name and last name
        System.out.print("Enter First Name: ");
        String firstName = scanner.next();
        
        System.out.print("Enter Last Name: ");
        String lastName = scanner.next();
        scanner.close();
        // Create Email object
        Email email = new Email(firstName, lastName);
        
        // Display user info
        System.out.println(email.showInfo());
    }
}
