# Library Management System

A desktop-based Library Management System developed using Java Swing, JDBC, and MySQL.

## Features

* User Login Authentication
* Student Registration
* Add New Books
* Issue Books
* Return Books
* MySQL Database Integration
* Customized User Interface
* Input Validation for Student Registration

## Technologies Used

* Java
* Java Swing
* JDBC
* MySQL
* Git
* GitHub

## Project Structure

* Student Registration Module
* Book Management Module
* Book Issue Module
* Book Return Module
* Login System
* Database Connectivity Module

## How to Run

1. Clone the repository.
2. Create the required MySQL database and tables.
3. Configure database credentials.
4. Open the project in NetBeans or IntelliJ IDEA.
5. Run the application.

## Screenshots

<img width="1920" height="1080" alt="Screenshot 2026-06-09 205540" src="https://github.com/user-attachments/assets/c6fbe225-de94-422d-8e86-f474d9d4b824" />
<img width="1920" height="1080" alt="Screenshot 2026-06-09 205548" src="https://github.com/user-attachments/assets/257d6817-047e-4b67-ad2d-6c1359bdfec1" />
<img width="1920" height="1080" alt="Screenshot 2026-06-09 205601" src="https://github.com/user-attachments/assets/aad747c1-1c46-47a9-a293-d79f9238e164" />
<img width="1920" height="1080" alt="Screenshot 2026-06-09 205712" src="https://github.com/user-attachments/assets/576deb84-1ce0-4e37-a6ff-fbfd966f40a0" />


















# Complete List of Contributions and Improvements

## 1. Added Due Date Validation (New Functionality)

### Problem

The Issue Book module allowed users to issue a book with a Due Date earlier than the Issue Date.

Example:

Issue Date: 09/06/2026

Due Date: 08/06/2026

This created invalid borrowing records.

### Implementation

* Parsed Issue Date and Due Date into Date objects.
* Compared both dates before issuing a book.
* Blocked the issue operation if Due Date < Issue Date.
* Displayed a validation message to the user.

### Result

Only logically valid borrowing periods can now be created.

---

## 2. Added Date Format Validation (New Functionality)

### Problem

The original application accepted invalid date values such as:

* 08/
* abc
* 12/06

because dates were stored as plain strings.

### Implementation

* Added date parsing using SimpleDateFormat.
* Added ParseException handling.
* Displayed a user-friendly validation message when invalid dates are entered.

### Result

Users must now enter dates in the correct format before a book can be issued.

---

## 3. Added Duplicate Student ID Validation (New Functionality)

### Problem

The Student Registration module allowed multiple students to be created with the same Student ID.

### Implementation

* Added a database lookup before INSERT.
* Checked whether the Student ID already exists.
* Blocked insertion if a duplicate record is found.
* Displayed an appropriate validation message.

### Result

Duplicate student records can no longer be created.

---

## 4. Added Duplicate Book ID Validation (New Functionality)

### Problem

The Add Book module allowed multiple books to be created with the same Book ID.

### Implementation

* Added a database lookup before INSERT.
* Checked whether the Book ID already exists.
* Blocked insertion if a duplicate is found.
* Displayed an error message to the user.

### Result

Duplicate book records can no longer be inserted.

---

## 5. Fixed Return Book Workflow Validation Bug

### Problem

While testing the Return Book module, I found an inconsistency involving the Book ID and Student ID fields.

The workflow validates:

txtbookid

but the error handling was:

* Showing a Student ID-related message.
* Moving focus to txtstudentid.

Even though the return operation is actually based on Book ID.

### Implementation

* Corrected the validation flow.
* Updated the logic so validation behavior aligns with txtbookid.
* Removed the mismatch between txtbookid validation and txtstudentid error handling.

### Result

The Return Book workflow now correctly guides users through the Book ID-based return process.

---

## 6. UI Customization and Asset Replacement

### Implementation

* Replaced original images.
* Replaced icons.
* Updated login screen visuals.
* Updated home screen visuals.
* Updated loading screen visuals.
* Adjusted image sizing and placement.
* Modified colors and layout elements.

### Result

The application now has a more customized appearance and is visually distinct from the original version.

---

## 7. Database Integration and Testing

### Implementation

Configured and tested:

* Login module
* Student Registration module
* Add Book module
* Issue Book module
* Return Book module
* JDBC connectivity
* MySQL integration

### Result

Verified that all major workflows execute correctly and interact properly with the database.

---

## 8. Git Version Control Integration

### Implementation

* Initialized a Git repository.
* Created commits for project changes.
* Learned and used Git workflows.
* Maintained project history.

### Result

Project changes are now version-controlled and recoverable.

---

## 9. GitHub Repository and Documentation

### Implementation

* Created a public GitHub repository.
* Added README documentation.
* Added screenshots.
* Added project description.
* Added technology tags.

### Result

The project is documented, version-controlled, and publicly accessible through GitHub for portfolio and interview purposes.

## Author

Lakshay
