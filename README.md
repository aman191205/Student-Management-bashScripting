# Student-Management-bashScripting

This project is a terminal-based Student Record Management System implemented entirely using **Bash scripting**. It provides a lightweight and efficient way to manage student academic records, including their marks, grades, and GPA. The system includes **user authentication**, **data persistence**, and multiple features tailored for both **teacher and student roles**. It is designed to operate in a UNIX-like environment and uses plain text files for data storage, avoiding any reliance on external databases or complex software dependencies.

## Table of Contents

* [System Features](#system-features)

  * [User Authentication](#user-authentication)
  * [Data Persistence](#data-persistence)
  * [Student Record Management (Teacher Functions)](#student-record-management-teacher-functions)
  * [Student Access (Student Functions)](#student-access-student-functions)
  * [Grade and GPA Calculation](#grade-and-gpa-calculation)
  * [Input Validation](#input-validation)
* [Technologies Used](#technologies-used)
* [Project Structure](#project-structure)
* [How to Run](#how-to-run)
* [Benefits](#benefits)

## System Features

### User Authentication

* Two types of users: **teacher** and **student**.
* Each user has hardcoded credentials.
* Only teachers can modify data; students have read-only access to their records.

### Data Persistence

* All student records are saved in a plain text file (`students.txt`) using a pipe-separated format.
* The system loads data from the file at startup and allows saving updated data during runtime.

### Student Record Management (Teacher Functions)

* **Add Student**: Input roll number, name, and marks for three subjects. The system calculates grades and GPA automatically.
* **Delete Student**: Remove a student record using the roll number.
* **Update Marks**: Change a student’s marks and update grades and GPA accordingly.
* **View Student**: View complete details of a single student including marks, grades, and GPA.
* **Display All Students**: Print a tabular view of all student records.
* **Sort by GPA**: Sort and display students in ascending or descending order of GPA.
* **List Passed & Failed**: Separate and display students based on a passing GPA threshold.

### Student Access (Student Functions)

* **View Grades**: Allows a student to view their marks, grades, and GPA.
* **View GPA Only**: Displays only the GPA for a specific roll number.

### Grade and GPA Calculation

* Grades are calculated based on a fixed scale:

  * **A**: 90+
  * **B**: 80–89
  * **C**: 70–79
  * **D**: 60–69
  * **F**: Below 60
* GPA is computed using grade-to-point mapping and credit hour weighting.

### Input Validation

* All numeric fields (marks and roll numbers) are validated to ensure non-negative integers.
* Prevents duplication of student roll numbers.
* Proper handling of missing or invalid input.

## Technologies Used

* **Bash scripting** (`.sh`)
* **bc** for floating point calculations
* **column** for formatting table outputs
* **File I/O** for data storage and retrieval

## Project Structure

* `students.txt`: File used to persist student data.
* `script.sh`: Main Bash script file containing all logic.
* No external dependencies or packages required.

## How to Run

1. Open a terminal in a UNIX/Linux environment.
2. Make the script executable:

   ```bash
   chmod +x script.sh
   ```
3. Run the script:

   ```bash
   ./script.sh
   ```

## Benefits

* Lightweight and efficient
* Terminal-based interface for simplicity and speed
* Secure, role-based access
* Completely self-contained—no need for external databases or packages

This project demonstrates how powerful and practical pure **Bash scripting** can be, even for building complete data management systems—simple, effective, and entirely terminal-based.
