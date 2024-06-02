# Doctor Appointment System

This repository contains the code for a Doctor Appointment System, which allows patients to book appointments with doctors, and for doctors to manage appointments and patient records.

## Prerequisites

### Technical Knowledge

Before setting up the application, you should have a basic understanding of:

- HTML
- CSS
- JavaScript (basics)
- PHP (Database connectivity)
- SQL queries

### Software Requirements

You will need to install the following software:

1. **XAMPP Server**
   - XAMPP is a free and open-source cross-platform web server solution stack package developed by Apache Friends, consisting mainly of the Apache HTTP Server, MariaDB database, and interpreters for scripts written in the PHP and Perl programming languages.
   - Download XAMPP from the official [Apache Friends website](https://www.apachefriends.org/index.html).

2. **phpMyAdmin**
   - phpMyAdmin is a free and open-source tool written in PHP, intended to handle the administration of MySQL over the Web. It can perform various tasks such as creating, modifying, or deleting databases, tables, fields, or rows; executing SQL statements; or managing users and permissions.
   - phpMyAdmin comes bundled with XAMPP.

3. **Text Editor**
   - Any text editor like Notepad++ or even the default Notepad will suffice for editing code files.

4. **Web Browser**
   - Any JavaScript-enabled web browser (such as Chrome, Firefox, or Edge) will be adequate for running and testing the application.

## Project Structure

The project is divided into two main parts: the backend and the frontend.

### Backend

The backend code is responsible for handling server-side operations and database interactions.

- `Admin.php`: Admin functionality
- `Ch_pass.php`: Change password
- `Login.html`: Login page
- `Logout.php`: Logout functionality
- `Patient.php`: Patient functionality
- `Patient_reg.php`: Patient registration
- `appointment.php`: Appointment handling
- `change_p.php`: Change password for users
- `connection.php`: Database connection
- `doc_delete.php`: Delete doctor
- `doctor.php`: Doctor functionality
- `doctor_mod.php`: Modify doctor details
- `doctor_reg.php`: Doctor registration
- `doctor_view.php`: View doctor details
- `history.php`: Patient history

### Frontend

The frontend code is responsible for the user interface and experience.

- `home.html`: Home page
- `about.php`: About page
- `admin.html`: Admin page
- `appointment.php`: Appointment booking page
- `contact.php`: Contact page
- `doctor.php`: Doctor page
- `doctor_login.php`: Doctor login
- `login.php`: User login
- `patient.php`: Patient page
- `patient_login.php`: Patient login
- `services.php`: Services offered
- `test.php`: Test page
- `view_app.php`: View appointments

## Setting Up the Application

1. **Start XAMPP**: Open the XAMPP control panel and start the Apache and MySQL modules.
2. **Create Database and Tables**: Use phpMyAdmin to create a new database (e.g., `doctor_appointment`). Import the SQL file (if available) to create necessary tables.
3. **Clone Repository**: Clone this repository into the `htdocs` directory of your XAMPP installation.
4. **Configure Database Connection**: Update the `database_con.php` file to configure the database connection details (such as database name, username, and password).
5. **Run the Application**: Open your web browser and navigate to `http://localhost/Doctor-Appointment-master/Frontend/home.html` to access the home page.

## Database Connection

Update the `database_con.php` file with your database connection details.

```php
<?php
$servername = "localhost";
$username = "root";
$password = "";
$database = "doctor_appointment";

// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);

// Check connection
if (!$conn) {
    die("Connection failed: " . mysqli_connect_error());
}
?>
