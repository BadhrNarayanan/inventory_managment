# Inventory Management System

This is a simple **Flask-based** project for managing categories in an inventory system. It allows you to:
- Add, update, and delete categories using a CRUD interface.
- Prevent duplicate categories with validation.
- Store data persistently using **SQLite**.

---

## Technologies Used
- Flask – Web framework  
- SQLAlchemy – ORM for database management  
- Bootstrap – For styling the web interface  
- dotenv – Environment variable management  

---

## Installation and Usage

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/inventory-management.git
```

### 2. Navigate into the Project Folder
```bash
cd inventory-management
```

### 3. Create and Activate a Virtual Environment
- On Windows:
```bash
python -m venv venv
venv\Scripts\activate
```
- On Linux/Mac:
```bash
python -m venv venv
source venv/bin/activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```

### 5. Set Environment Variables
Create a `.env` file in the project root and add the following:
```
SECRET_KEY=supersecretkey
SQLALCHEMY_DATABASE_URI=sqlite:///db.sqlite3
SQLALCHEMY_TRACK_MODIFICATIONS=False
DEBUG=True
```

### 6. Initialize the Database
Run the following commands to create the SQLite database:
```bash
flask db init
flask db migrate -m "Initial migration."
flask db upgrade
```

### 7. Run the App
Start the Flask server:
```bash
python main.py
```

Open your browser and visit:
```
http://127.0.0.1:5000
```

---

## Features

- Add new categories  
- Update existing categories  
- Delete categories  
- Avoid duplicate names with validation  
- Persistent data storage using SQLite  

---

## Project Structure
```
/inventory_management
 ├── /templates         # HTML templates  
 ├── /static            # CSS and JS files  
 ├── /models            # SQLAlchemy models  
 ├── main.py            # Flask application entry point  
 ├── config.py          # App configuration  
 ├── requirements.txt   # Python dependencies  
 ├── README.md          # Project documentation  
```

---

## Troubleshooting

- If you encounter `ImportError: cannot import name 'load_dotenv'`, ensure you have installed `python-dotenv`:
```bash
pip install python-dotenv
```

- If the server doesn't start, make sure your environment variables are correctly configured.
