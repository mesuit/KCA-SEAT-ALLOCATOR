Here is a **Professional yet Simple `README.md**` file.

It is written in "Developer Layman's Language"—meaning it explains **how to run the code** step-by-step without using overly complex jargon, so the person you hand this project to can set it up easily.

**Copy the code below and save it as `README.md` in your project folder.**

---

```markdown
# 🎓 KCA University Exam Seat Allocator

**A Smart Exam Management System for Universities.** *Automates student registration, exam scheduling, seat allocation, and generates QR-coded exam dockets.*

---

## 🚀 Project Overview
This system solves the chaos of manual exam planning. instead of using Excel sheets, this app allows:
1.  **Students** to register themselves and pick their units.
2.  **Admins** to create exams and assign rooms.
3.  **The System** to automatically allocate seats (preventing collisions).
4.  **Generation of PDF Dockets** with QR codes for exam entry.

---

## 🛠 Tech Stack
* **Backend:** Python (Django 5.0)
* **Database:** SQLite (Local) / PostgreSQL (Production)
* **Frontend:** Bootstrap 5 (Responsive HTML/CSS)
* **PDF Generation:** html2pdf.js
* **QR Codes:** Python `qrcode` library

---

## 💻 Installation Guide (How to Run Locally)

Follow these steps to get the project running on your computer.

### **1. Clone the Repository**
Download the code to your machine.
```bash
git clone [https://github.com/sesco001/KCA-SEAT-ALLOCATOR.git](https://github.com/sesco001/KCA-SEAT-ALLOCATOR.git)
cd KCA-SEAT-ALLOCATOR

```

### **2. Create a Virtual Environment**

This keeps your project dependencies separate from your computer.

```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate

```

### **3. Install Dependencies**

Install all the required tools (Django, QR code generator, etc.).

```bash
pip install -r requirements.txt

```

### **4. Set Up the Database**

Create the database tables.

```bash
python manage.py makemigrations
python manage.py migrate

```

### **5. Create an Admin User (The "Guru")**

You need this account to manage exams and students.

```bash
python manage.py createsuperuser

```

* *Username:* `admin`
* *Password:* `admin123` (or whatever you choose)

### **6. Run the Server**

Start the application.

```bash
python manage.py runserver

```

> **Success!** Open your browser and go to: `http://127.0.0.1:8000/`

---

## 📖 How to Use the System

### **Step 1: Admin Setup (The Foundation)**

*Before students can do anything, the Admin must set up the university structure.*

1. Go to `http://127.0.0.1:8000/admin/` and log in.
2. **Add Rooms:** Create venues (e.g., "Hall 4", Capacity: 50).
3. **Add Courses:** Create units (e.g., "SWE 101 - Intro to Software").
4. **Create Exams:** Link a Course to a Room and set a Date.

### **Step 2: Student Registration**

1. Go to the **Home Page**.
2. Click **Student Portal** -> **Register**.
3. Enter details (e.g., Reg No: `23/0400`).
4. **Select Units:** Use the "Select All" feature to pick semester units.

### **Step 3: The Magic (Seat Allocation)**

1. Once the Admin creates an Exam for a unit the student selected, the system **automatically assigns a seat**.
2. The student goes to the Home Page -> **Check Exam Seat**.
3. They enter their Reg Number.
4. **Result:** A printable PDF Docket showing the **Seat Number** and **QR Code**.

---

## 📂 Project Structure

* `core/` - The main logic (Views, Models, URLs).
* `templates/` - The HTML files (Frontend).
* `static/` - CSS and Javascript files.
* `manage.py` - The command center for running the app.

---



*For educational and project demonstration purposes.*

```

```
