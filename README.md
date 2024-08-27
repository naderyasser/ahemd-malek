# Documentation for ScholarSyncApi

## Introduction
This documentation provides information on setting up, configuring, and running a simple Flask-based web application for user authentication using Google OAuth2. The application allows users to sign up, log in using their Google accounts, and view their profile information. The technologies used include Flask, SQLAlchemy for database management, and Google OAuth2 for authentication.

## Prerequisites
Before running the application, ensure the following dependencies are installed:

- Python
- Flask
- Flask-SQLAlchemy
- Google Auth Library

Install the required packages using the following command:
```bash
pip install Flask Flask-SQLAlchemy google-auth
```

## Configuration
1. Replace the `your_secret_key_here` placeholder in the `app.secret_key` with a secure secret key.
2. Configure your Google OAuth2 credentials:
   - `CLIENT_ID`: Replace with your Google OAuth2 client ID.
   - `CLIENT_SECRET`: Replace with your Google OAuth2 client secret.
   - `REDIRECT_URI`: The URI to redirect to after successful Google authentication.

## Database Configuration
The application uses SQLite by default for simplicity. Modify the `app.config['SQLALCHEMY_DATABASE_URI']` field for a different database configuration.

## Running the Application
To run the application, execute the following command in the terminal:
```bash
python your_app_filename.py
```

Access the application at `http://127.0.0.1:30/`.

## Routes
- `/`: Home page with a welcome message and a login link.
- `/login`: Login page.
- `/logingoogle`: Redirects to Google OAuth2 authentication.
- `/sign_up`: Sign-up page.
- `/signup`: Handles user registration from the sign-up page.
- `/callback`: Callback route for Google OAuth2 authentication.
- `/img/<int:img_id>/`: Displays profile images using the `Img` model.

## Models
### Users
- `id`: User ID (primary key).
- `name`: User's name.
- `password`: User's password.
- `email`: User's email (unique).
- `age`: User's age.
- `profile_img`: User's profile image.
- `birthdate`: User's date of birth.
- `phone_number`: User's phone number.
- `father_number`: User's father's phone number.
- `city`: User's city.
- `academic_year`: User's academic year.
- `academic_section`: User's academic section.
- `created_at`: Timestamp of user creation.

### Img
- `id`: Image ID (primary key).
- `code`: Image code.
- `img`: Binary data for the image.

## Author
[Your Name]

Feel free to customize the application to meet your requirements. For questions or assistance, please open an issue in the repository.
