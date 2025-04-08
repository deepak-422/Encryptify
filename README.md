# Password Encryption and Decryption System

A C++ application that encrypts and decrypts passwords using the Caesar cipher. The program stores the encrypted passwords in a MySQL database, and users can sign up or log in to the system through a command-line interface.

## Features:
- **Signup**: Encrypts the password and stores it in the MySQL database.
- **Login**: Decrypts the stored password and checks if it matches the user's input.
- **Simple Command-Line Interface** for user interaction.

## Requirements:
- **MySQL**: A MySQL server must be set up.
- **C++ Compiler**: A C++ compiler (like `g++`) is needed.
- **MySQL Client Library**: The MySQL connector for C++.

## Setup Instructions:
1. Clone the repository:
   ```bash
   git clone https://github.com/deepak-422/Encryptify.git
Set up MySQL Database:

Ensure MySQL is installed and running.

Create a database mydb and a password table:

sql
Copy
CREATE DATABASE mydb;

USE mydb;

CREATE TABLE password (
    Id VARCHAR(255) PRIMARY KEY,
    PW VARCHAR(255) NOT NULL
);
Compile and Run:

Compile your C++ code using the following command:

bash
Copy
g++ main.cpp -o password_system -lmysqlclient
Run the compiled program:

bash
Copy
./password_system
How to Use:
1: Signup by entering a new ID and password. The password is encrypted before being stored in the database.

2: Login with your ID and password. The program will decrypt the password and compare it to the stored one.

0: Exit the program.

Encryption:
The passwords are encrypted using a Caesar cipher (a simple encryption method) with a shift of 3.

License:
This project is licensed under the MIT License - see the LICENSE file for details.
