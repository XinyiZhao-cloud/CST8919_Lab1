# CST8919 Lab 1 – Flask Authentication with Auth0

## Student Information

Name: Xinyi Zhao  
Course: CST8919  
Lab: Lab 1 – Implementing User Login with Flask and Auth0

---

## Project Overview

This project demonstrates how to integrate Auth0 authentication into a Flask web application.

The application allows users to:

- Log in using Auth0
- View authenticated user information
- Log out securely
- Access a protected page that requires authentication

Auth0 acts as the Identity Provider (IdP), while the Flask application acts as the Service Provider (SP).

---

## Video Demonstration

**YouTube Video:**

https://youtu.be/S1l01S-nJuw 

The video demonstrates:

- Auth0 login
- Auth0 logout
- Protected route access
- Code walkthrough
- Key concepts learned

---

## Features

### Authentication

- User Login
- User Logout
- User Profile Display

### Protected Route

A custom protected route was added:

` /protected `

Behavior:

- Authenticated users can access the page.
- Unauthenticated users are redirected to the login page.

---

## Technologies Used

- Python 3
- Flask
- Auth0
- HTML/CSS

---

## Project Structure
```text
auth0-flask-app/
│
├── app.py
├── auth.py
├── requirements.txt
├── .env
├── .gitignore
│
├── templates/
│   ├── index.html
│   └── protected.html
│
└── static/
    └── style.css
```
---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/XinyiZhao-cloud/CST8919_Lab1/tree/main

cd auth0-flask-app 
```
### 2. Create a Virtual Environment
```bash
python3 -m venv venv 
```

**Activate the virtual environment:**
```source 
venv/bin/activate 
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt 
```

### 4. Configure Auth0

**Create a .env file in the project root.**

Example:
```env
AUTH0_CLIENT_ID=YOUR_CLIENT_ID 
AUTH0_CLIENT_SECRET=YOUR_CLIENT_SECRET 
AUTH0_DOMAIN=YOUR_DOMAIN 
APP_SECRET_KEY=YOUR_SECRET_KEY 
AUTH0_REDIRECT_URI=http://127.0.0.1:5000/callback 
```
### 5. Configure Auth0 Application Settings

In the Auth0 Dashboard:

**Allowed Callback URLs**

`http://127.0.0.1:5000/callback `

**Allowed Logout URLs**

`http://127.0.0.1:5000 `

**Allowed Web Origins**

`http://127.0.0.1:5000 `

### 6. Run the Application

```bash 
python app.py 
```
**Open:**

`http://127.0.0.1:5000 `

---

## Testing

### Login

1. Open the application.
2. Click Login.
3. Authenticate through Auth0.
4. Confirm that user information is displayed.

### Logout

1. Click Logout.
2. Confirm that the session is terminated.

### Protected Route

**Visit:**

`http://127.0.0.1:5000/protected `

**Expected behavior:**

- Logged-in users can access the page.
- Non-authenticated users are redirected to the login page.

---

## What I Learned

Through this lab I learned how to:

- Integrate Auth0 with Flask
- Configure authentication callbacks
- Manage user sessions
- Protect routes using authentication
- Configure environment variables securely
- Deploy authentication features using a third-party Identity Provider