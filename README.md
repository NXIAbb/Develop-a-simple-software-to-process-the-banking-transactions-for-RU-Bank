Download link :https://programming.engineering/product/develop-a-simple-software-to-process-the-banking-transactions-for-ru-bank/


# Develop-a-simple-software-to-process-the-banking-transactions-for-RU-Bank
Develop a simple software to process the banking transactions for RU Bank
Your team will develop a simple software to process the banking transactions for RU Bank. The transactions will be entered through the command lines on the terminal. The software is an interactive system to produce the output whenever a transaction is entered. The software shall be able to process transactions of opening an account, closing an existing account, depositing money to an existing account, withdrawing money from an existing account, and print the details of all accounts. RU Bank provides four types of banking accounts listed in the table below. Note that, same person can hold different types of accounts, however, cannot hold a College Checking and Checking at the same time. For all account types, must be age of 16 or older to open, for College Checking, must be under the age of 24 to open. The interest rates and monthly fees are different based on the account types and account options.

CS 213 Fall2023 Project #2 – 150 points Dr. Lily Chang

Savings class, extends the Account class; includes one instance variable only, and defines the constants for

interest rate and fee. protected boolean isLoyal; //loyal customer status

MoneyMarket class, extends the Savings class; includes one instance variable only, and defines the constants for interest rate and fee. private int withdrawal; //number of withdrawals

You MUST include the Java classes below. -5 points for each class missing or NOT used.

Date class. Reuse the code from your Project 1.

Profile class. Define the profile of an account holder as follows. You cannot add additional instance variables. -2 points for each violation.

public class Profile implements Comparable<Profile>{ private String fname;

private String lname;

private Date dob;

}

AccountDatabase class. An instance of this class is a linear data structure using an array to hold a list of accounts with different types. The initial capacity of the array is 4. The capacity will be automatically increased by 4 whenever the array is full. You must implement and use the methods listed and you cannot add additional instances variable or change the signatures of the methods. -2 points for each violation.

public class AccountDatabase {

private Account [] accounts; //list of various types of accounts private int numAcct; //number of accounts in the array

private int find(Account account) {} //search for an account in the array private void grow() //increase the capacity by 4

public boolean contains(Account account){} //overload if necessary

public boolean open(Account account){} //add a new account

public boolean close(Account account){} //remove the given account

public boolean withdraw(Account account){} //false if insufficient fund

public void deposit(Account account){}

public void printSorted(){} //sort by account type and profile public void printFeesAndInterests(){} //calculate interests/fees public void printUpdatedBalances(){} //apply the interests/fees

}

TransactionManager class. This is the user interface class that processes the transactions entered on the terminal and performs all Input/Ouput. This class handles all Java exceptions and invalid data before it calls the methods in AccountDatabase class to complete the transactions. For example, InputMismatchException, NumberFormatException, NoSuchElementException, invalid dates of birth, invalid campus codes, and invalid amounts. Whenever there is an exception or invalid data, display a message on the terminal. See the Project2ExpectedOutput.txt for the proper messages to display. -2 points for each exception not caught or invalid data not checked in this class or messages not displayed. You must include a run() method to process the command lines. You will lose 5 points for not including this method, or the method exceed 40 lines.

RunProject2 class as the driver to run Project 2.

JUnit test classes. Write code to test the following methods.

• isValid() method in the Date class, 5 invalid cases, 2 valid cases.

• close() method in the AccountDatabase class, with 1 true case and 1 false case.

4



Class Diagram. Create a class diagram to document your software structure for Project 2. Hand-drawing the diagram is not acceptable, and you’ll lose 15 points. You can follow the links below to create a class diagram online and save it to your device as a picture, which can be included in your submission. You can also use other UML tools if you like. For each rectangle (class), include the instance variables and public methods. NO need to include the constants and private methods. DO NOT INCLUDE the test classes and the Java library classes in the diagram.

http://draw.io/ à Create New Diagram à UML à Class Diagram

https://online.visual-paradigm.com/app/diagrams/ à Create New à Class Diagram

You are required to generate the Javadoc after you properly commented your code. Your Javadoc must include the documentations for the constructors, private methods, and public methods of all Java classes. Generate the Javadoc in a single folder and include it in the zip file to be submitted to Canvas. Please double check your Javadoc after you generated it by opening the index.html file in the folder, and ensure the descriptions are NOT EMPTY. You will lose points if any description in the Javadoc is empty. You will lose 5 points for not including the Javadoc.
