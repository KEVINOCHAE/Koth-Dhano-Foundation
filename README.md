# Koth-Koth-Foundation Website

This repository contains the source code for the Koth Dhano Foundation web application.
The system was developed using Python and uses PostgreSQL as the database.
Project Structure

Rusken-Charitable-Foundation/
│
├── app/                 # Main application modules
├── instance/            # Instance-specific configurations
├── migrations/          # Database migration scripts
├── app.py               # Application entry point
├── config.py            # Application configuration
├── requirements.txt     # Python dependencies
├── wsgi.py              # WSGI entry point for deployment
└── README.md
Requirements
Before running the application, ensure the following are installed:
Python 3.9+
PostgreSQL
pip (Python package manager)
virtualenv (recommended)
Installation
1. Clone or extract the project

git clone <repository-url>
cd Koth-Dhano-Foundation
Or extract the provided project archive.

2. Create a virtual environment
python -m venv venv
Activate it:
Windows

venv\Scripts\activate
Linux / Mac
source venv/bin/activate

3. Install dependencies
pip install -r requirements.txt

Environment Configuration
Create a .env file in the root directory and configure the required environment variables.
Example:

SECRET_KEY=your_secret_key
DATABASE_URL=postgresql://username:password@localhost:5432/database_name

MAIL_SERVER=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your_email@example.com
MAIL_PASSWORD=your_email_password
Adjust the values according to your hosting environment.
Database Setup
Create a PostgreSQL database and update the DATABASE_URL accordingly.
If migrations are available, initialize the database:

flask db upgrade
Running the Application

Start the development server using:
python app.py
or
flask run

The application will be available at:

http://127.0.0.1:5000

Deployment
The application can be deployed using any Python-compatible hosting platform such as:
Railway
Render
DigitalOcean
VPS with Gunicorn + Nginx
For production deployments, configure the WSGI entry point:
wsgi.py

Notes
Environment variables must be configured before running the application.
Ensure the PostgreSQL database is accessible from the hosting environment.
Email configuration should be updated with valid SMTP credentials.
Support
This package contains the application source code required to deploy the Rusken Charitable Foundation website on a new hosting environment.
Any infrastructure or hosting configuration should be managed by the new deployment environment