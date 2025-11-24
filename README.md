# Campus Course & Records Manager (CCRM) 🎓

Welcome to the **Campus Course & Records Manager (CCRM)**\! This isn't just a console app; it's a full-fledged attempt to simulate how a university manages its brain—the data. I built this project to move beyond simple "Hello World" scripts and create something robust that handles students, courses, grades, and file storage, all while keeping the data safe.

## 🚀 Project Overview

The main idea behind CCRM was to take the Java concepts I’ve learned—from basic loops to advanced file I/O—and put them to work in a real-world scenario.

**Here’s what this system can actually do:**

  * **Student Central:** It’s a complete directory. I can add new students, update their details, or deactivate records when they graduate.
  * **Course Control:** Administrators can create courses, assign instructors, and manage the curriculum.
  * **The Registrar Logic:** This is the cool part—it handles enrollments. It checks if a student has exceeded their credit limit before letting them sign up. It also calculates GPAs automatically (so no manual math\!).
  * **Real-World Storage:** Instead of losing data when the console closes, I used **Java NIO.2** to save everything to CSV files. It’s fast and persistent.
  * **Safety First:** I built a backup system that uses recursive directory operations to timestamp and save copies of the data. Better safe than sorry\!
  * **Data crunching:** It generates system reports so you can see a snapshot of the university's performance.

-----

## ☕ A Quick Look at Java's Journey

To appreciate why I used certain features, it helps to look at how Java got here. It’s come a long way since the 90s\!

  * **The 90s (Java 1.0 - 1.2):** It started with the promise of "Write Once, Run Anywhere." Then came the big split into Standard (SE), Enterprise (EE), and Micro (ME) editions.
  * **The Game Changer (Java 5, 2004):** This release brought us Generics and the enhanced for-loop, making code much cleaner.
  * **The Modern Era (Java 8, 2014):** This is my favorite update. It introduced **Lambda expressions** and the **Streams API**, which allows for functional programming (you'll see a lot of this in my code\!).
  * **Recent History (Java 9 - 21):** From modularizing the JDK to the latest "Virtual Threads" in Java 21, the language is faster and more lightweight than ever.

-----

## 🏗️ Architecture: How It Runs

If you are new to the Java ecosystem, it can be a bit alphabet-soup-ish. Here is how the pieces fit together:

1.  **JDK (The Toolkit):** This is what I used to build CCRM. It has the compiler (`javac`) and tools.
2.  **JRE (The Playground):** This provides the libraries and environment to run the app.
3.  **JVM (The Magic Translator):** This is why Java works on Windows, Mac, and Linux. It takes my compiled code and translates it for your specific machine.

-----

## 🛠️ Getting Started

Want to run this on your machine? Here is the drill.

### Prerequisites

  * **Java 8** or higher (I recommend 17 or 21).
  * Your favorite IDE (IntelliJ, Eclipse, VS Code).
  * A terminal/command prompt.

### Installation & Run Guide

**1. Get the code:**

```bash
git clone <repository-url>
cd campus-course-records-manager
```

**2. Compile it:**
If you are doing it the "hard way" (manual compilation):

```bash
javac -d . src/main/java/com/ccrm/*.java src/main/java/com/ccrm/**/*.java
```

**3. Launch it:**

```bash
java com.ccrm.CampusCourseRecordsManager
```

### 🖥️ Eclipse Setup (For IDE users)

If you prefer clicking over typing commands:

1.  Open Eclipse -\> **File \> Import**.
2.  Select **Git \> Projects from Git**.
3.  Paste the repo URL, select the `main` branch, and finish.
4.  Find `CampusCourseRecordsManager.java`, right-click, and **Run As \> Java Application**.

-----

## 🔍 Under the Hood: Mapping Concepts to Code

This project was a requirement for the "Build Your Own Project" module, so I made sure to map specific coding concepts to actual files. Here is where you can find the "good stuff":

<img width="1536" height="2048" alt="image" src="https://github.com/user-attachments/assets/5d3e0819-41c8-419a-9e52-18fd78cd1fe4" />


  * **Encapsulation:** Check out `model/Student.java`. All fields are private, protecting the data integrity.
  * **Inheritance & Polymorphism:** I created a base class called `Person`. Both `Student` and `Instructor` inherit from it, which lets me treat them interchangeably in certain lists.
  * **Design Patterns:**
      * **Singleton:** Look at `DataStore.java`. It ensures we only have *one* database instance running in memory.
      * **Builder:** In `CourseBuilder.java`, I use this pattern to construct complex objects step-by-step.
  * **Modern Java (Java 8+):**
      * **Streams:** In `services/StudentService.java`, I use streams to filter and process student lists efficiently.
      * **NIO.2:** `utils/FileUtils.java` uses the modern `Path` and `Files` libraries (instead of the old `File` class).
  * **Error Handling:** I didn't just use generic errors; I wrote custom exceptions like `MaxCreditLimitExceededException` to handle specific business logic failures.

### 🐛 Pro-Tip: Debugging with Assertions

I added some internal consistency checks using assertions. To enable them (and see if I broke anything logic-wise), run the app with the `-ea` flag:

```bash
java -ea com.ccrm.CampusCourseRecordsManager
```
