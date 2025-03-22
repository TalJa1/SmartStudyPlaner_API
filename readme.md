# Smart Study Planner API

## Overview
Smart Study Planner API is a backend service built with FastAPI to help students organize their study plans, manage schedules, and track academic progress. The application uses SQLite as its database to store user data and study information.

## Features
- User authentication and management
- Study plan creation and organization
- Schedule tracking and reminders
- Progress monitoring and analytics
- Course and assignment management

## Tech Stack
- **FastAPI**: Modern, high-performance web framework
- **SQLite**: Lightweight database
- **SQLAlchemy**: SQL toolkit and ORM
- **Pydantic**: Data validation and settings management
- **JWT**: Authentication and authorization

## Getting Started

### Prerequisites
- Python 3.8+
- pip

### Installation
1. Clone the repository
   ```
   git clone https://github.com/yourusername/SmartStudyPlaner_API.git
   cd SmartStudyPlaner_API
   ```

2. Create a virtual environment
   ```
   python -m venv venv
   venv\Scripts\activate
   ```

3. Install dependencies
   ```
   pip install -r requirements.txt
   ```

4. Run the application
   ```
   uvicorn app.main:app --reload
   ```

5. Access the API documentation at http://localhost:8000/docs

## Project Structure
```
SmartStudyPlaner_API/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── database.py
│   ├── models/
│   ├── schemas/
│   ├── routes/
│   ├── services/
│   └── utils/
├── tests/
├── .env
├── requirements.txt
└── README.md
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login and get access token

### Users
- `GET /api/users/me` - Get current user information
- `PUT /api/users/me` - Update user information

### Study Plans
- `GET /api/plans` - Get all study plans
- `POST /api/plans` - Create a new study plan
- `GET /api/plans/{plan_id}` - Get a specific study plan
- `PUT /api/plans/{plan_id}` - Update a study plan
- `DELETE /api/plans/{plan_id}` - Delete a study plan

### Schedules
- `GET /api/schedules` - Get all schedules
- `POST /api/schedules` - Create a new schedule
- `GET /api/schedules/{schedule_id}` - Get a specific schedule
- `PUT /api/schedules/{schedule_id}` - Update a schedule
- `DELETE /api/schedules/{schedule_id}` - Delete a schedule

## Development

### Running Tests
```
pytest
```

### Database Migrations
```
alembic upgrade head
```

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contributors
- [Your Name](https://github.com/yourusername)