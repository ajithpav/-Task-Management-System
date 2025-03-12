# Task Management System with Location Tracking

## Overview
This is a Django-based **Task Management System** that allows users to:
- **Register and log in** with their details.
- **Add and manage tasks** with status tracking.
- **Assign tasks** to users.
- **Track user and task locations** using geolocation (latitude & longitude).
- **View personal profile details**.

## Features
✅ **User Registration & Login**  
✅ **Task Creation with Date & Time**  
✅ **Task Status (Pending/Completed) Based on Date**  
✅ **Geolocation Support (Converts Address to Latitude & Longitude)**  
✅ **Dashboard for Task Management**  
✅ **User Profile Page**  

## Tech Stack
- **Backend:** Django (Python)
- **Database:** SQLite (default) / Can be switched to PostgreSQL or MySQL
- **Geolocation:** GeoPy (ArcGIS geocoding API)
- **Frontend:** HTML, CSS, Bootstrap

## Installation & Setup

### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/task-management.git
cd task-management
```

### **2. Create & Activate a Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate     # On Windows
```

### **3. Install Dependencies**
```bash
pip install -r requirements.txt
```

### **4. Apply Migrations & Start the Server**
```bash
python manage.py migrate
python manage.py runserver
```

### **5. Access the Application**
- Open your browser and go to: `http://127.0.0.1:8000`

## API Endpoints & Routes
| Route | Method | Description |
|--------|--------|--------------------------------|
| `/register/` | GET, POST | Register a new user |
| `/login/` | GET, POST | User login |
| `/dashboard/` | GET | View all tasks |
| `/add_task/` | GET, POST | Add a new task |
| `/my_profile/` | GET | View logged-in user profile |

## Usage
### **Register a New User**
1. Go to `/register/` and enter your details (name, email, mobile, password, address).
2. The system will automatically convert your address to latitude and longitude.

### **Log In**
1. Go to `/login/` and enter your email and password.
2. If correct, you will be redirected to the dashboard.

### **Add a Task**
1. Go to `/add_task/` and enter:
   - Task Name
   - Date & Time
   - Assigned User
   - Address
2. The system will:
   - Convert the address into latitude & longitude.
   - Set task status automatically:
     - **Pending** (if today or future date)
     - **Completed** (if past date)

### **View Dashboard & Tasks**
- The `/dashboard/` page will show all created tasks.

### **View Profile**
- `/my_profile/` will show the logged-in user's details.

## Dependencies
Install required packages using:
```bash
pip install -r requirements.txt
```
Key dependencies:
- **Django** (Backend framework)
- **GeoPy** (Geolocation API for address conversion)
- **Bootstrap** (Frontend styling)

## Future Enhancements
- ✅ Task Filtering & Search
- ✅ User Role Management (Admin, Employee, Manager)
- ✅ Email Notifications for Assigned Tasks
- ✅ Interactive Map for Task Locations

## License
This project is **MIT Licensed**. Feel free to modify and use it as needed.

---
Made with ❤️ using Django 🚀

