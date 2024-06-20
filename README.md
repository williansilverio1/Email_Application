Email Application README

Overview

This Java application is designed to manage email accounts for employees in a company. It generates email addresses based on the employee's name and department, creates random passwords, and allows setting mailbox capacity and alternate emails.

Features

- Email Generation: Automatically creates an email address based on the employee's first name, last name, and department.
- Password Generation: Generates a random password for the user.
- Mailbox Capacity Management: Allows setting and retrieving the mailbox capacity.
- Alternate Email Management: Allows setting and retrieving an alternate email.
- Password Management: Allows changing and retrieving the password.
- Display Information: Displays employee's full name, company email, and mailbox capacity.

Classes

1. Email
This class handles the main functionalities of the application including email and password generation, and storing user details.

Attributes

- firstName (String): Employee's first name.
- lastName (String): Employee's last name.
- password (String): Employee's password.
- department (String): Department of the employee.
- email (String): Generated email address.
- mailboxCapacity (int): Capacity of the mailbox in MB (default is 500MB).
- defaultPasswordLength (int): Default length of the generated password (default is 10 characters).
- alternateEmail (String): Alternate email address.
- companySuffix (String): Company domain suffix (default is "company.com").

Methods

- Email(String firstName, String lastName): Constructor to initialize first name, last name, department, and generate email and password.
- private String setDepartment(): Asks the user to select a department and returns the corresponding department name.
- private String randomPassword(int length): Generates a random password of given length.
- public void setMailboxCapacity(int capacity): Sets the mailbox capacity.
- public void setAlternateEmail(String altEmail): Sets the alternate email address.
- public void changePassword(String password): Changes the current password.
- public int getMailboxCapacity(): Retrieves the mailbox capacity.
- public String getAlternateEmail(): Retrieves the alternate email address.
- public String getPassword(): Retrieves the current password.
- public String showInfo(): Displays the employee's name, email, and mailbox capacity.

2. EmailApp
This class contains the main method to run the application.

Methods

- public static void main(String[] args): Entry point of the application. Creates an instance of the `Email` class and displays the user information.

How to Run

1. Compile the Java classes:
   
   javac emailapp/Email.java emailapp/EmailApp.java

2. Run the application:
   
   java emailapp.EmailApp

3. Follow the prompts to enter the department code for the new employee.

Example Usage


New worker: Willian. Department Codes:
1 for Sales
2 for Development
3 for Accounting
0 for none
Enter department code: 1
Your password is: A1B2C3D4E5
DISPLAY NAME: Willian Silva
COMPANY EMAIL: willian.silva@Sales.company.com
MAILBOX CAPACITY: 500mb

Customization

- Change Password Length: Modify the defaultPasswordLength attribute in the Email class.
- Company Domain Suffix: Change the companySuffix attribute in the Email class.
- Mailbox Capacity: Use the setMailboxCapacity(int capacity) method to change the default mailbox capacity.

Dependencies

- Java Development Kit (JDK) 8 or higher.

License

This project is licensed under the MIT License.
