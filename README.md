Student Fee & Information Management System


A web-based application built using Python Flask to manage student data, course registrations, and fee transactions. The system provides role-based access control for Administrators, Accountants, and Students to ensure secure and organized data management.

🚀 Features
1. User Roles & Authentication
Secure Login/Logout: Session-based authentication for all users.

Role-Based Access Control (RBAC): Distinct dashboards and permissions for Admins, Accountants, and Students.

Password Management: Functionality for all users to change their passwords securely.

2. Admin Module
Manage Accountants: Register, view, edit, and delete accountant profiles.

Manage Students: Register, view, edit, and delete student profiles.

Manage Courses: Add new courses to students and remove existing ones.

Fee Management: Record fee deposits and view transaction history.

Profile Management: Update admin details and upload/change profile photos.

3. Accountant Module
Manage Students: Register new students and view student lists.

Course & Fee Management: Add courses to students and process fee deposits.

Transaction History: View all financial transactions recorded in the system.

Profile Management: Update personal contact details.

4. Student Module
Personal Dashboard: View personal profile details.

Academic Financials:

View enrolled courses.

Track total fees, amount paid, and due balance.

View detailed transaction history (deposits).

🛠️ Tech Stack
Backend: Python, Flask

Database: MySQL (accessed via pymysql in mylib.py)

Frontend: HTML, CSS, Jinja2 Templates

File Handling: Werkzeug (for secure image uploads)

📂 Database Structure
The application relies on the following database tables (inferred from the code):

logindata: Stores email, password, and user type.

admindata: Admin personal details.

accountantdata: Accountant personal details.

studentdata: Student personal details.

photodata: Stores paths for uploaded admin photos.

coursedata: Maps students to courses and fees.

transactiondata: Records fee payments and transaction methods.

⚙️ Installation & Setup
Clone the repository:

Bash

git clone https://github.com/yourusername/student-management-system.git
cd student-management-system
Install dependencies: Ensure you have Python installed, then run:

Bash

pip install flask pymysql
Database Configuration:

Import the SQL schema into your MySQL database.

Configure the database connection in mylib.py (ensure host, user, password, and database name are correct).

Run the Application:

Bash

python app.py
Access the App: Open your browser and navigate to: http://127.0.0.1:5000/

📁 Project Structure
Plaintext

├── app.py              # Main Flask application logic
├── mylib.py            # Database connection and helper functions
├── static/
│   └── images/         # Folder for uploaded images
├── templates/          # HTML Templates (Jinja2)
│   ├── Welcome.html
│   ├── Login.html
│   ├── AdminHome.html
│   ├── StudentHome.html
│   └── ... (other templates)
└── README.md
🛡️ Security
Sessions: Uses Flask session for maintaining user state.

File Security: Uses secure_filename to prevent path traversal attacks during file uploads.

SQL Injection Prevention: Note: Ensure all raw SQL queries in the code are parameterized to prevent injection vulnerabilities.

🤝 Contributing
Fork the repository.

Create a new branch (git checkout -b feature-branch).

Commit your changes.

Push to the branch.

Open a Pull Request.

Created by [Kunal Maheshwari]
