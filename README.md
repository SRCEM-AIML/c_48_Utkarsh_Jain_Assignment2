# c_48_Utkarsh_Jain_Assignment2
# Student Project

A simple Django web application with Docker and Jenkins integration.

## Overview

This project is a basic Django application with two apps that demonstrates containerization with Docker and CI/CD using Jenkins.

## Features

- Simple web application with Bootstrap UI
- Home page and sample page navigation
- Docker containerization
- Continuous Integration and Deployment with Jenkins

## Project Structure

```
StudentProject/
├── app1/                  # Main app with home page
├── app2/                  # Secondary app with sample page
├── StudentProject/        # Project configuration
├── db.sqlite3             # SQLite database
├── dockerfile             # Docker configuration
├── Jenkinsfile            # Jenkins CI/CD pipeline
├── manage.py              # Django management script
└── requirements.txt       # Python dependencies
```

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/SRCEM-AIML/c_48_Utkarsh_Jain_Assignment2.git
   cd StudentProject
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Run migrations:
   ```
   python manage.py migrate
   ```

5. Start the development server:
   ```
   python manage.py runserver
   ```

6. Access the application at `http://127.0.0.1:8000/`

## Docker Usage

Build and run the Docker container:

```
docker build -t utkarsh2005/django-docker .
docker run -p 8000:8000 --name studentproject utkarsh2005/django-docker
```

## CI/CD Pipeline

This project uses Jenkins for continuous integration and deployment:

1. Pipeline clones the repository
2. Builds a Docker image
3. Pushes the image to Docker Hub

## Pages

- Home page: `/`
- Sample page: `/app2/sample/`

## Technologies Used

- Django 5.1.7
- Bootstrap 5
- Docker
- Jenkins
- SQLite
