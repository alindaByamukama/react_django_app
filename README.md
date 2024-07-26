# React & Django - Notes App

A full-stack notes application built with React.js for the frontend and Django for the backend. This app allows users to create, view, update, and delete notes.

## Table of Contents

- [Features](#features)
- [Upcoming Features](#upcoming-features)
- [Installation](#installation)
- [Usage](#usage)
- [Navigation](#navigation)

## Features

- **Create Notes:** Add new notes with a title and content.
- **View Notes:** See a list of all your notes.
- **Delete Notes:** Remove notes you no longer need.
- **Backend:** Django REST framework API for managing notes.
- **Frontend:** React.js for a dynamic and responsive user interface.

## Upcoming Features
- **Update Notes:** Edit the content of your existing notes.
- **Page Navigation:** Move with ease throughout the app.
- **Landing Page:** Understand what the app is about and how to get started.

## Installation

### Prerequisites

- Python 3.x
- Node.js
- npm (Node Package Manager)
- Django
- React

### Backend Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/alindaByamukama/react_django_app.git
    cd react_django_app/backend
    ```
    
2. Create a virtual environment and activate it (outside both backend and frontend direcotires):
    ```bash
    python -m venv venv
    source venv/bin/activate
    ```

3. Update the backend settings:
   ```bash
    DATABASES = {
         "default": {
         "ENGINE": "django.db.backends.sqlite3",
         "NAME": BASE_DIR / "db.sqlite3",
    }
   ```
   
4. Remove (delete) the Procfile and the .choreo directory.

5. Install dependencies:
    ```bash
    cd backend/
    pip install -r requirements.txt
    ```

6. Run migrations:
    ```bash
    python manage.py migrate
    ```
    
7. Start the Django development server:
    ```bash
    python manage.py runserver
    ```

### Frontend Setup

1. Navigate to the frontend directory (you may split the terminal to have both running):
    ```bash
    cd ../frontend
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Create a `.env` file in the `frontend` directory and add your environment variables. Example:
    ```bash
    REACT_APP_API_URL="http://127.0.0.1:8000/"
    ```
   
4. Remove (delete) the apiUrl from the api.js file and set the baseUrl to:
  ```bash
  const api = axios.create({
    baseURL: import.meta.env.VITE_API_URL,
  })
  ```

5. Start the React development server:
    ```bash
    npm run dev
    ```

## Usage
Access the app at http://localhost:5173 (frontend) and http://127.0.0.1:8000 (backend).
Or alternatively you may visit the app at this (address)[https://65710196-84f1-452f-8740-db919e4febca.e1-us-east-azure.choreoapps.dev]. 
(NB: Not always running due to server availability.)
    
## Navigation

Currently, navigation is rudimentary and can be done via the address bar. Example:
- `http://[address]/register` to register a new user.
- `http://[address]/login` to login and create, view or delete your notes.
- `http://[address]/logout` to logout.
