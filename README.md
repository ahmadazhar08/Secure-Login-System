# Secure Login System

A simple secure login web application built with Python and Flask.

## Features

- User registration and login
- Password hashing using Argon2
- Password validation
- Parameterized SQLite queries for SQL injection protection
- Session-based authentication
- Logout functionality
- Simple web interface

## Technologies Used

- Python
- Flask
- SQLite
- Argon2
- HTML and CSS

## Project Structure

```text
Secure-Login-System/
├── app.py
├── requirements.txt
├── .gitignore
├── README.md
└── templates/
    ├── base.html
    ├── login.html
    ├── register.html
    └── dashboard.html
```

## How to Run

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Open http://127.0.0.1:5000 in your browser.

## Security Concepts

Passwords are never stored as plain text. Argon2 creates a password hash before it is stored.

SQL queries use parameters instead of directly joining user input into SQL statements. This helps protect against SQL injection.

Flask sessions are used to keep track of authenticated users after login.

## Testing

1. Register a new user.
2. Try a weak password.
3. Register with a strong password.
4. Log in with the correct password.
5. Try an incorrect password.
6. Open the dashboard after login.
7. Click logout.

## Note

This is an educational internship project. A production application should also use HTTPS, CSRF protection, rate limiting, secure secret management, and stronger deployment settings.
