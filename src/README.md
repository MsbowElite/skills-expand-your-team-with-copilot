# Mergington High School Activities

A FastAPI-based web application that allows students to view and sign up for extracurricular activities at Mergington High School, with teacher authentication for managing registrations.

## Features

### For Students
- View all available extracurricular activities
- Search activities by name or description
- Filter activities by:
  - Category (Sports, Arts, Academic, Community, Technology)
  - Day of the week (Monday-Sunday, including weekend activities)
  - Time of day (Before School, After School, Weekend)
- View activity details including schedule, description, max participants, and current participants

### For Teachers
- Login with teacher credentials
- Register students for activities (requires authentication)
- Unregister students from activities (requires authentication)
- View all registered participants for each activity

## Technology Stack

- **Backend**: FastAPI with Uvicorn server
- **Database**: MongoDB for persistent data storage
- **Frontend**: Vanilla JavaScript, HTML, and CSS
- **Authentication**: Password hashing with SHA-256 for teacher accounts

## API Endpoints

### Activities
- `GET /activities` - Get all activities with optional filtering by day, start_time, and end_time
- `GET /activities/days` - Get a list of all days that have activities scheduled
- `POST /activities/{activity_name}/signup` - Register a student for an activity (requires teacher authentication)
- `POST /activities/{activity_name}/unregister` - Remove a student from an activity (requires teacher authentication)

### Authentication
- `POST /auth/login` - Login with teacher credentials
- `GET /auth/check-session` - Verify if a session is valid

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
