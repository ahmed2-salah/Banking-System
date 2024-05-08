# Banking-System
Banking system using the client-server model to establish connection between two machines  as a server and client using Tcp socket.


## Client Model 
**1. Main Program (main.cpp):**
*Entry point of the application.
* Handles user input to determine whether the user is a regular user or an admin.
* Instantiates UserManager or AdminManager based on user input.
* Manages the login process and user interactions.
* Exits the application when the user chooses to exit.


 **2. Client Class (client.h, client.cpp):**
* Base class for UserManager and AdminManager.
* Defines pure virtual functions for handling account-related operations such as
  *  getting the account number.
  *  viewing account details.
  *  viewing transaction history.
  *  sending requests to the server.
  *  performing login.
* Contains a method to clear the console screen.

**3. UserManager Class (user.h, user.cpp):**
* Inherits from Client class.
* Implements user-specific functionalities such as:
  *  transferring accounts.
  *  making transactions.
  *  viewing account details.
  *  viewing transaction history.
  *  logging in.
* Manages the client-side communication with the server.

**4. AdminManager Class (admin.h, admin.cpp):**
Inherits from Client class.
Implements admin-specific functionalities such as viewing account details, getting account numbers, viewing bank database, creating new users, deleting users, updating user data, viewing transaction history, and logging in.
Manages the client-side communication with the server.
Header Files:
client.h, user.h, and admin.h contain class declarations.
They include necessary Qt and C++ headers for networking, input/output operations, and data handling.
Source Files:
client.cpp, user.cpp, and admin.cpp contain the implementations of the respective classes.
They include implementations for methods defined in the header files and handle networking, user input/output, and server communication.
Qt Framework Dependencies:
The project relies on the Qt framework for networking (QTcpSocket), data serialization/deserialization (QDataStream), signal-slot mechanism, and other functionalities provided by Qt classes.
This hierarchy outlines the structure of the project, with clear separation of concerns between different classes responsible for handling user interactions, server communication, and business logic.
