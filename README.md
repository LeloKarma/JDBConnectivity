# LogReg

LogReg is a simple JavaFX application that provides a login and registration functionality using a MySQL database. 
This application allows users to log in with their username and password, and also provides a registration feature to create new user accounts.

## Database Setup

To use this application, you need to set up a MySQL database and configure the necessary tables. 
Follow the steps below to create the required database and table:

1. Install and set up MySQL on your system if you haven't already.

2. Create a new database called "person" by executing the following SQL query:
   ````sql
   CREATE DATABASE person;
   ```

3. Switch to the "person" database:
   ````sql
   USE person;
   ```

4. Create the "users" table with the following schema:
   ````sql
   CREATE TABLE users (
       id INT PRIMARY KEY AUTO_INCREMENT,
       username VARCHAR(50) NOT NULL,
       password VARCHAR(50) NOT NULL
   );
   ```

## Running the Application

To run the application, follow these steps:

1. Make sure you have Java and JavaFX installed on your system.

2. Compile the Java source code using your preferred method (e.g., command line, IDE).

3. Ensure that the MySQL server is running.

4. Update the connection details in the `LogReg` class:

    - Set the `DATABASE_URL` variable to the URL of your MySQL database (e.g., "jdbc:mysql://localhost:3306/person").
    - Set the `USERNAME` variable to your MySQL username.
    - Set the `PASSWORD` variable to your MySQL password.

5. Run the compiled Java class `LogReg` using the `java` command or your preferred IDE.

6. The application window titled "Login" will open.

## Usage

### Login

1. Enter your username and password in the respective fields.

2. Click the "Login" button.

3. If the provided username and password match an entry in the database,
 an information alert will be displayed with the message "Login Successful" and a welcome message.
 Otherwise, an error alert will be displayed with the message "Login Failed" and an invalid username or password message.

### Registration

1. Enter a desired username and password in the respective fields.

2. Click the "Register" button.

3. If the registration is successful and the user is added to the database,
  an information alert will be displayed with the message "Registration Successful" and a success message.
  Otherwise, an error alert will be displayed with the message "Registration Failed" and an error message.

Note: The application assumes a single-user environment. If you want to extend it to support multiple users, 
you would need to modify the database schema and update the application logic accordingly.

## Dependencies

The application has the following dependencies:

- JavaFX: The JavaFX library is used for the graphical user interface components.
- MySQL Connector/J: The MySQL Connector/J library is used to connect to the MySQL database.

Make sure to include these dependencies in your project build path or dependency management system.

---

That's all you need to know to use this LogReg application. If you have any issues or questions, feel free to reach out.
