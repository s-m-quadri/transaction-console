# Transaction Console

The "Transaction Console" is a command-line interface (CLI) application developed entirely in C that simulates a transaction process similar to that of an ATM. It provides users with a console-based environment to perform various transaction-related operations, as part of a project conducted by the Deogiri Institute of Engineering and Management Studies for the "Design and Analysis of Algorithms" subject.


                       **                         
                    ** ** **                      
                 ***        ***                   
              ***              ***                
           ***                    ***             
        ***                          ***          
     *** ** ************************ ** ***       
                                                  
        ****    ****         ****   ****          
         **      **           **     **           
         **      **           **     **           
         **      **           **     **           
         **      **           **     **           
         **      **           **     **        
        ****    ****         ****   ****          
                                                  
       **********************************         
     **************************************       

## Table of Contents

1. [Features](#1-features)
2. [Getting Started](#2-getting-started)
3. [Usage](#3-usage)
4. [Documentation](#4-documentation)
5. [Walk Through](#5-walk-through)

## 1. Features

&crarr; [back to index](#table-of-contents)

Here are the key aspects and functionalities of the "Transaction Console":

1. **Command-Line Interface (CLI):** The application is accessed through a command-line interface, allowing users to interact with it by typing commands and receiving corresponding responses.

2. **Cross-Platform Support:** The "Transaction Console" is designed to work on both Windows and Linux operating systems, ensuring compatibility and accessibility for a wide range of users.

3. **ASCII Color Codes:** The application incorporates ASCII color codes to enhance the visual aesthetics of the console interface. This feature adds a touch of visual appeal to the user experience.

4. **Command Recognition:** The console is capable of recognizing and interpreting commands entered by the user. It can understand and process various transaction-related commands without relying on regular expressions. If a command is not recognized, the console gracefully ignores it.

5. **Error Handling:** The "Transaction Console" includes error handling capabilities to ensure a smooth user experience. It provides informative error messages in case of incorrect inputs or exceptional situations, allowing users to understand and rectify their actions.

6. **Offline Functionality:** The application operates entirely offline and doesn't require any local file storage. This ensures that users can perform transactions and access the features of the "Transaction Console" without relying on an internet connection or external data sources.

7. **Optimization with Greedy Approach:** The "Transaction Console" incorporates a Greedy Approach to solve a specific problem statement related to maximizing denominations in a currency system. It intelligently chooses the best available option at each step to optimize the utilization of given denominations and fill the remaining amount effectively.

Overall, the "Transaction Console" offers a user-friendly and efficient environment for simulating transaction processes. It combines the power of the C programming language, CLI interactivity, error handling, offline functionality, and optimization techniques to provide a comprehensive solution for transaction-related operations.

Happy transacting with the "Transaction Console"!

## 2. Getting Started

&crarr; [back to index](#table-of-contents)

To get started with the **Transaction Console**, follow these steps:

1. Head to the latest release in this repository.

2. Download the executable file for your operating system (Windows or Linux) from the release page.

3. Once the file is downloaded, you can directly execute it without the need for any compilation or building steps. The executable file contains the compiled version of the "Transaction Console" application.

4. Open a command-line interface (CLI) or terminal on your computer.

5. Navigate to the location where you saved the downloaded executable file.

6. Execute the "Transaction Console" application by running the appropriate file. Refer to usage section for more info.

7. The console interface will appear, ready for you to enter commands and perform transaction-related operations.

8. If you ever need help or want to learn more about the available commands and their usage, simply type the command `help` in the console. The application will provide you with detailed information about each command and guide you through the process.

## 3. Usage

&crarr; [back to index](#table-of-contents)

Please note that the "Transaction Console" already provides the compiled executable file for your convenience. It eliminates the need for manual compilation or building steps, allowing you to quickly start using the application.

All you need to do is run the appropriate executable file.

    Just Double click for windows users

For linux users, simply run

    ./Linux64_Transaction_Console.out 

Also you can compile the code (if needed) in the **src** folder.

    gcc cs50.c bank.c token.c main.c -o Linux64_Transaction_Console.out
    
can do (optionally) memory check using

    valgrind ./Linux64_Transaction_Console.out 

or (optionally) time check using

    time ./Linux64_Transaction_Console.out 

## 4. Documentation

&crarr; [back to index](#table-of-contents)

- **help**: Use the `help` command to display information and guidance on using the "Transaction Console". It provides an overview of the available commands and their usage.

```
    Command $: help
```

- **login**: Use the `login` command to initiate the login process. Upon entering this command, the console will prompt you to enter your login credentials, such as a username and password. Successful login will grant you access to perform transaction-related operations.

```
    Command $: login
```

- **deposit**: Use the `deposit (amount)` command to deposit a specified amount into the logged-in account. Replace `(amount)` with the desired amount to be deposited. For example, to deposit 300 into the account, enter the command `$: deposit 300`. The deposited amount will be added to the balance of the logged-in account.

```
    Command $: deposit (amount)
    e.g.    $: deposit 300
```

- **withdraw**: Use the `withdraw (amount)` command to withdraw a specified amount from the logged-in account. Replace `(amount)` with the desired amount to be withdrawn. For example, to withdraw 300 from the account, enter the command `$: withdraw 300`. The specified amount will be deducted from the balance of the logged-in account.

```
    Command $: withdraw (amount)
    e.g.    $: withdraw 300
```

- **withdraw cash**: Use the `withdraw cash (amount) (note-denom...) done` command to withdraw a specified amount from the logged-in account in the form of cash. Replace `(amount)` with the desired amount to be withdrawn. Additionally, specify the preferred note denominations in decreasing order of preference, separated by spaces. For example, `$: withdraw cash 300 100 50 done` will withdraw 300 from the account using notes of denomination 100 and 50, prioritizing the maximum utilization of these notes. The console will calculate the optimal (minimum) number of notes required to fulfill the withdrawal amount and provide them to you.

```
    Command $: withdraw cash (amount) (note-denom...) done
    e.g.    $: withdraw cash 300 100 50 done
```

- **show**: Use the `show` command to display the status of the logged-in account. It will show information such as the account holder's name, current balance, and any other relevant details.

```
  Command $: show
```

- **logout**: Use the `logout` command to initiate the logout process. Upon entering this command, the console will log out the current user and return to the login screen, allowing another user to log in if needed.

```
  Command $: logout
```

- **exit**: Use the `exit` command to terminate the console and exit the application. Entering this command will close the console interface and end the "Transaction Console" session.

```
  Command $: exit
```

Please note that all commands should be entered exactly as shown, including any required arguments and in the correct order. Refer to the command descriptions above for proper usage.


## 5. Walk Through

&crarr; [back to index](#table-of-contents)

1. **Dashboard of Transaction Console:** Dashboard of Transaction Console displaying the initial prompt for the bank name. After entering the bank name, it welcomes the user to the console interface.

![TC-Interface.png](img/TC-Interface.png)

2. **Executed Help Command:** Output of the executed Help command displaying the information and usage instructions for the available commands in the "Transaction Console".

![TC-Intro.png](img/TC-Intro.png)

3. **Login, Deposit, Withdraw, Show Status, and Logout:** Various commands available in the "Transaction Console" including Login, Deposit, Withdraw, Show Status, and Logout. Each command enables the user to perform specific actions within the transaction system.

![TC-1st-Tour.png](img/TC-1st-Tour.png)

4. **Login, Show Status, Withdraw (with denomination using greedy), Show Status, Logout:** Step-by-step demonstration of the transaction process. It showcases logging into the system, displaying the account status, making a withdrawal with denominations using a greedy approach, showing the updated account status, and finally logging out from the console.

![TC-2nd-Tour.png](img/TC-2nd-Tour.png)

5. **Error Handling Demonstration:** Demonstration of error handling in the "Transaction Console". Examples include accessing the console without logging in, typing an incomplete command like deposit without specifying the amount, and typing a wrong command like "abcd" which is ignored gracefully by the console.

![TC-Error-Handling.png](img/TC-Error-Handling.png)


## Thanks for visiting
