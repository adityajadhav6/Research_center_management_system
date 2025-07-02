# Research Center Management System

The **Research Center Management System** is a simple web app built to help manage everything related to a research center. Whether it's supervisors, research scholars, advisory committees, publications, patents, or grants, this system has got you covered. It’s designed to be user-friendly, making it easy for admins, supervisors, and viewers to interact with and manage the data efficiently.

---

## Features

- **User Authentication**: Login functionality for administrators and viewers.
- **Supervisor Management**: Add, edit, delete, and view supervisors.
- **Research Scholars**: Manage research scholars under supervisors.
- **Advisory Committee**: Manage advisory committee members.
- **Publications**: Manage books, book chapters, journals, and conferences.
- **Patents**: Manage published and granted patents.
- **Grants**: Manage faculty and student grants.
- **Role-Based Access**: Different access levels for administrators and viewers.

---

## Prerequisites

1. **MAMP**: Install MAMP for running the project locally.
2. **PHP**: Ensure PHP is installed (comes with MAMP).
3. **MySQL**: Use MySQL for the database (comes with MAMP).

---

## Installation Steps

1. **Install MAMP**:
   - Download and install MAMP from [https://www.mamp.info/](https://www.mamp.info/).

2. **Set Up the Project**:
   - Navigate to the `htdocs` directory in your MAMP installation:
     ```
     Applications > MAMP > htdocs
     ```
   - Place the `Research_center_management_system` folder inside the `htdocs` directory.

3. **Start MAMP**:
   - Open MAMP and start the servers (Apache and MySQL).

4. **Database Setup**:
   - Open `phpMyAdmin` by navigating to [http://localhost:8888/phpmyadmin](http://localhost:8888/phpmyadmin).
   - Create a new database named `research_centre`.
   - Import the SQL file:
     - Go to the `Import` tab in `phpMyAdmin`.
     - Select the file `sql/setup.sql` from the project directory.
     - Click `Go` to execute the SQL script.

5. **Configure Database Connection**:
   - Ensure the database connection details in `db/connection.php` match your MAMP setup:
     ```php
     $servername = "localhost";
     $username = "root";
     $password = "root"; // Default password for MAMP
     $dbname = "research_centre";
     $port = 8889; // Default MySQL port for MAMP
     ```

6. **Access the Application**:
   - Open your browser and navigate to [http://localhost:8888/Research_center_management_system](http://localhost:8888/Research_center_management_system).

---

## Usage

### Login
- **Admin Login**:
  - Username: `admin`
  - Password: `admin123` (hashed using MD5 in the database).
- **Viewer Login**:
  - No password required. Click the "Login as Viewer" button.

### Features Overview
1. **Supervisors**:
   - Add, edit, delete, and view supervisors.
   - View research scholars under each supervisor.

2. **Research Scholars**:
   - Add, edit, and delete research scholars.

3. **Advisory Committee**:
   - Manage advisory committee members.

4. **Publications**:
   - Manage books, book chapters, journals, and conferences.

5. **Patents**:
   - Manage published and granted patents.

6. **Grants**:
   - Manage faculty and student grants.

---

## File Structure

- **`index.php`**: Main dashboard for the application.
- **`login.php`**: Login page for administrators and viewers.
- **`db/connection.php`**: Database connection file.
- **`sql/setup.sql`**: SQL script to set up the database schema.
- **`Supervisor.php`**: Manage supervisors and advisory committee.
- **`fetch_research_scholars.php`**: View research scholars under a supervisor.
- **`publications.php`**: Manage publications (books, book chapters, journals, conferences).
- **`patents.php`**: Manage patents (published and granted).
- **`grants.php`**: Manage grants (faculty and student).
- **`css/style.css`**: Stylesheet for the application.

---

## Troubleshooting

1. **Database Connection Issues**:
   - Ensure the database credentials in `db/connection.php` are correct.
   - Verify that the MySQL server is running in MAMP.

2. **Missing Tables**:
   - Re-import the `sql/setup.sql` file into the `research_centre` database.

3. **Permission Issues**:
   - Ensure the `htdocs` folder and its contents have the correct permissions.

---

## Future Enhancements

- Add password hashing for better security.
- Implement CSRF protection for forms.
- Add pagination for large datasets.
- Enhance the UI with modern frameworks like Bootstrap.

---

## License

This project is for educational purposes only.