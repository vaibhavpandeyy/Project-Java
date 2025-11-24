# Project Statement: Campus Course & Records Manager (CCRM)

## 1. Problem Statement
Managing the core data of an educational institution—student records, course catalogs, enrollments, and grades—is a complex task. Many institutions still rely on fragmented systems or manual data entry, which leads to redundancy, data loss, and calculation errors (such as incorrect GPAs or over-enrollment). There is a critical need for a centralized, robust, and automated system to manage these academic records efficiently while ensuring data persistence and integrity.

## 2. Scope of the Project
The **Campus Course & Records Manager (CCRM)** is a comprehensive Java-based console application designed to digitize and automate the academic administration process.

* **In-Scope:**
    * **Core Data Management:** Full CRUD (Create, Read, Update, Delete/Deactivate) operations for Students and Courses.
    * **Business Logic:** Automated calculations for GPAs and enforcement of academic rules (e.g., credit limits per semester).
    * **Data Persistence:** Implementation of a custom file-based storage system using Java NIO.2 (CSV format) to ensure data survives application restarts.
    * **System Maintenance:** Utilities for automated timestamped backups and system health reporting.

* **Out-of-Scope:**
    * Graphical User Interface (GUI) or Web Interface.
    * Integration with external SQL databases (this project focuses on file manipulation).
    * Financial/Tuition processing modules.

## 3. Target Users
* **Academic Registrars:** Who need to process student enrollments, enforce credit limits, and generate academic transcripts.
* **University Administrators:** Who are responsible for maintaining the course catalog, defining curriculum structures, and assigning instructors.
* **System Auditors:** Who require access to system reports and backup logs to ensure data integrity.

## 4. High-Level Features
* **Student Lifecycle Management:** Tools to register new students, update their personal details, and manage their active/inactive status.
* **Course & Curriculum Control:** Functionality to create courses, define credit values, and assign instructors.
* **Smart Enrollment Engine:** A logic layer that validates enrollments against rules (e.g., preventing students from exceeding max credit limits).
* **Automated Grading System:** Built-in calculation of Grade Point Averages (GPA) based on completed coursework.
* **Robust File System Integration:**
    * **Import/Export:** Seamless loading and saving of data to CSV files.
    * **Safety Net:** A recursive backup utility that creates timestamped copies of the data directory.
* **Analytics & Reporting:** Generation of comprehensive system reports (e.g., total enrollment stats, grade distributions).
