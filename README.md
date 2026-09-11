# 🚲 EcoGlide — Smart Mobility Management Platform

[🇮🇹 Versione italiana](README.it.md)

**Smart Mobility Management Platform built with Django and Django REST Framework**

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-Web%20Framework-green?logo=django&logoColor=white)
![Django REST Framework](https://img.shields.io/badge/DRF-REST%20API-red)
![JWT](https://img.shields.io/badge/Auth-JWT-orange)

## Project Overview

EcoGlide is an academic software engineering project focused on the design and implementation of a smart mobility and vehicle-sharing management platform.

The system provides a Django-based backend with REST APIs for managing users, shared vehicles, rides, urban areas, maintenance reports and mobility-related services.

The project also includes frontend dashboards for different user roles and a set of simulated external services used to demonstrate routing, weather and payment workflows.

## Main Features

- User and role management
- JWT-based authentication
- Shared vehicle management
- Ride creation and lifecycle management
- Urban area and restricted-zone management
- Vehicle maintenance reports
- Operator and public-administration dashboards
- Usage and mobility analytics
- CO₂ savings statistics
- Revenue and ride statistics
- Simulated routing services
- Simulated weather information
- Mock payment processing

## Tech Stack

- Python
- Django
- Django REST Framework
- Simple JWT
- SQLite
- HTML
- CSS
- JavaScript

## Architecture

The project is organized around a Django backend and a lightweight frontend.

```text
sals-ingegneria/
├── config/
│   ├── settings.py
│   └── urls.py
├── mobility/
│   ├── models.py
│   ├── serializers.py
│   ├── services.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── frontend_app/
│   ├── index.html
│   ├── dashboard_operatore.html
│   └── dashboard_pa.html
├── manage.py
├── requirements.txt
├── README.md
├── README.it.md
└── .gitignore
```

## Simulated Services

Some integrations are intentionally implemented as local simulations or mocks for academic purposes.

### Routing

The routing component generates routes while accounting for restricted urban areas.

It does not rely on an external routing provider and should be considered a simulated routing service rather than a production navigation engine.

### Weather

Weather information is generated locally for demonstration purposes and does not use a live weather API.

### Payments

Payment operations are simulated through a mock gateway and do not process real financial transactions.

These components were designed so that real third-party providers could be integrated in a production-oriented implementation.

## Installation

Clone the repository:

```bash
git clone https://github.com/zSpiDa/EcoGlide.git
cd EcoGlide
```

Create a virtual environment.

### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Apply database migrations:

```bash
python manage.py migrate
```

Optionally populate the database with sample data:

```bash
python manage.py seed_db
```

Start the backend server:

```bash
python manage.py runserver
```

The API will be available at:

```text
http://127.0.0.1:8000/
```

The frontend files can be opened from the `frontend_app/` directory.

Make sure the frontend API base URL points to:

```text
http://127.0.0.1:8000/api
```

## Running the Tests

Run the Django test suite with:

```bash
python manage.py test
```

## Academic Context

EcoGlide was developed as an academic project for the **Software Engineering** course.

The project focuses on software architecture, REST API design, domain modelling and the implementation of a mobility-management workflow using Django.

## Disclaimer

Routing, weather and payment services are simulated for educational purposes and are not intended for production use.
