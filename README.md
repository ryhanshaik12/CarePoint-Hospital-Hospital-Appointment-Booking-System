# CarePoint-Hospital-Hospital-Appointment-Booking-System
A Django-based hospital appointment booking system

A web-based hospital appointment booking application built with **Python and Django**. The project provides separate workflows for patients and doctors, allowing patients to book appointments and doctors to manage appointment statuses through a dedicated dashboard.

## Features

### Patient Features
- Patient registration and login
- Browse available doctors
- Book hospital appointments
- View personal appointment history
- Prevent duplicate bookings for the same doctor, date, and time
- Cancel personal appointments

### Doctor Features
- Secure doctor login
- Dedicated doctor dashboard
- View appointments assigned to the logged-in doctor
- Approve pending appointments
- Mark appointments as completed
- Cancel appointments

### Database
- Store patient account information
- Maintain doctor profiles and specializations
- Store appointment details, including date, time, reason, and status
- Use SQLite for local development

## Technologies Used

- **Programming Language:** Python
- **Web Framework:** Django
- **Database:** SQLite
- **Frontend:** HTML and CSS
- **Version Control:** Git and GitHub

## Project Structure

```text
carepoint-hospital/
├── appointments/
│   ├── migrations/
│   ├── templates/
│   ├── models.py
│   ├── views.py
│   ├── forms.py
│   ├── admin.py
│   └── urls.py
├── config/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── templates/
├── manage.py
├── requirements.txt
├── .gitignore
└── README.md
```

*The structure above is representative; your actual folders and files may differ.*

## Getting Started

Follow these steps to run the project locally.

### Prerequisites

- Python installed on your computer
- Git (optional, if cloning the repository)

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd carepoint-hospital
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with the URL of your GitHub repository.

Alternatively, download the repository as a ZIP file and extract it.

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply Database Migrations

```bash
python manage.py migrate
```

### 5. Create an Administrator Account (Optional)

```bash
python manage.py createsuperuser
```

Follow the prompts to create the account.

### 6. Start the Development Server

```bash
python manage.py runserver
```

## Appointment Statuses

| Status | Description |
|---|---|
| Pending | Appointment is awaiting a doctor's decision |
| Approved | Appointment has been approved |
| Completed | Appointment has been marked completed |
| Cancelled | Appointment has been cancelled |

## Learning Outcomes

This project provided practical experience with:

- Django models, views, forms, and URL routing
- User authentication and role-based access checks
- CRUD operations and relational database models
- Form validation and duplicate appointment-slot checks
- Database migrations and SQLite
- Git and GitHub project management

## Security and Limitations

- This is an educational project intended for learning and portfolio demonstration.
- It is not intended for production use with real patient information.
- Production deployment would require additional security, privacy, testing, and operational safeguards.
- The project uses SQLite for local development.
- Appointment-slot validation is application-level and may require stronger database-level protection against simultaneous booking requests.

## Future Improvements

Possible future enhancements include:

- Email notifications for appointment updates
- Doctor availability and scheduling management
- Improved automated testing
- Production deployment with secure configuration


If you find this project useful, feel free to explore the repository and its implementation.
