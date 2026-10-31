
# Patient Management System API | FastAPI

## Project Overview

The **Patient Management System API** is a backend application developed using FastAPI and Python. It provides RESTful API endpoints to manage patient records, retrieve patient information, create new patient entries, update existing records, delete patient data, and sort patients based on different parameters.

The application uses a JSON file (`patients.json`) for storing and managing patient records. It also uses Pydantic models for data validation and automatically calculates the Body Mass Index (BMI) of patients based on their height and weight.

This project demonstrates practical implementation of FastAPI concepts, including API routing, HTTP methods, request validation, exception handling, query parameters, path parameters, and JSON-based data persistence.

## Project Highlights

- **Patient Record Management:** Create, view, update, and delete patient records.
- **BMI Calculation:** Automatically calculates BMI using patient height and weight.
- **BMI Classification:** Generates a health category based on the calculated BMI.
- **Data Validation:** Uses Pydantic models to validate patient information.
- **Patient Search:** Retrieve individual patient records using their unique patient ID.
- **Patient Sorting:** Sort patient records based on height, weight, and BMI.
- **JSON Data Storage:** Stores patient information in a local JSON file.
- **Exception Handling:** Handles invalid patient IDs, duplicate records, and invalid sorting parameters.
- **RESTful API:** Implements GET, POST, PUT, and DELETE methods.
- **API Documentation:** Supports interactive API documentation through FastAPI Swagger UI.

## Technologies Used

- **Python** – Core programming language.
- **FastAPI** – Framework for building RESTful APIs.
- **Pydantic** – Data validation and model creation.
- **JSON** – Patient data storage.
- **Uvicorn** – ASGI server for running the FastAPI application.

## Project Structure

```text
Fastapi-project/
│
├── Main.py
├── patients.json
└── README.md
```

### File Description

- **Main.py:** Contains the FastAPI application, Pydantic models, BMI calculation, API endpoints, and patient management operations.
- **patients.json:** Stores patient records in JSON format.
- **README.md:** Documentation of the project.

## API Endpoints

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Welcome message |
| GET | `/about` | API information |
| GET | `/view` | View all patient records |
| GET | `/patient/{patient_id}` | Retrieve a specific patient |
| GET | `/sort` | Sort patients by height, weight, or BMI |
| POST | `/create` | Create a new patient |
| PUT | `/edit/{patient_id}` | Update patient information |
| DELETE | `/delete/{patient_id}` | Delete a patient record |

## Key Functionalities

### 1. Patient Data Validation

Uses Pydantic BaseModel to validate patient information, including:

- Patient ID
- Name
- City
- Age
- Gender
- Height
- Weight

Validation rules include positive age, valid gender values, and positive height and weight.

### 2. BMI Calculation

The application automatically calculates BMI using the following formula:

BMI = Weight (kg) / Height (m)²

The calculated BMI is rounded to two decimal places.

### 3. BMI Classification

The application generates a verdict based on the calculated BMI.

- Below 18.5 – Underweight
- 18.5 to below 25 – Normal
- 25 to below 30 – Overweight
- 30 and above – Obese

### 4. Patient Sorting

Patients can be sorted using the following parameters:

- Height
- Weight
- BMI

Sorting supports both ascending and descending orders.

### 5. CRUD Operations

The API supports complete CRUD operations:

- **Create:** Add new patient records.
- **Read:** Retrieve all or individual patient records.
- **Update:** Modify existing patient information.
- **Delete:** Remove patient records.

### 6. Error Handling

The application handles different error conditions using FastAPI HTTPException, including:

- Patient not found (404).
- Duplicate patient ID (400).
- Invalid sorting field (400).
- Invalid sorting order (400).

## Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/Aman-Pathak1302/Fastapi-project.git
```

### Step 2: Navigate to the Project Directory

```bash
cd Fastapi-project
```

### Step 3: Create a Virtual Environment

```bash
python -m venv venv
```

### Step 4: Activate Virtual Environment

For Windows:

```bash
venv\Scripts\activate
```

### Step 5: Install Required Libraries

```bash
pip install fastapi uvicorn pydantic
```

### Step 6: Run the Application

```bash
uvicorn Main:app --reload
```

## Access API Documentation
After starting the server, open the following URLs in your browser:
- **API Base URL:** http://127.0.0.1:8000
- **Swagger UI:** http://127.0.0.1:8000/docs
- **ReDoc:** http://127.0.0.1:8000/redoc

Swagger UI provides an interactive interface to test all available API endpoints.

## Learning Outcomes
Through this project, I gained practical experience in:

- Building RESTful APIs using FastAPI.
- Understanding backend development fundamentals.
- Working with Pydantic models and data validation.
- Implementing CRUD operations.
- Handling HTTP requests and responses.
- Using path parameters and query parameters.
- Implementing exception handling.
- Working with JSON files for data storage.
- Performing automatic calculations using computed fields.
- Testing APIs through Swagger UI.

## Future Improvements
- Integrate a relational database such as PostgreSQL or MySQL.
- Implement user authentication and authorization.
- Add advanced patient search and filtering.
- Improve API security and data protection.
- Implement automated API testing.
- Add pagination for large patient datasets.
- Deploy the application to a cloud platform.




