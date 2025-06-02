# AI-Powered Personalized Learning Platform

This file contains instructions for testing and validating the learning platform functionality.

## Testing the Backend API

1. Navigate to the backend directory:
   ```
   cd /home/ubuntu/learning_platform/backend
   ```

2. Start the backend server:
   ```
   npm run dev
   ```

3. Test the following API endpoints:
   - `GET /api/auth/register` - Register a new user
   - `POST /api/auth/login` - Login with user credentials
   - `GET /api/courses` - Get all courses
   - `GET /api/courses/:id` - Get a specific course with lessons

## Testing the Frontend

1. Navigate to the frontend directory:
   ```
   cd /home/ubuntu/learning_platform/frontend
   ```

2. Start the frontend development server:
   ```
   npm start
   ```

3. Test the following pages and features:
   - User registration and login
   - Dashboard with course recommendations
   - Course listing and filtering
   - Course details and lesson navigation
   - AI Learning Assistant integration
   - Personalized recommendations

## Testing Docker Deployment

1. From the project root directory:
   ```
   cd /home/ubuntu/learning_platform
   ```

2. Build and start the containers:
   ```
   docker-compose up --build
   ```

3. Access the application:
   - Frontend: http://localhost
   - Backend API: http://localhost:5000

4. Verify all functionality works as expected in the containerized environment.

## Validation Checklist

- [ ] Backend API endpoints return expected responses
- [ ] User authentication (register/login) works correctly
- [ ] Course listing and details display properly
- [ ] Lesson content is accessible and navigable
- [ ] AI Learning Assistant component is functional
- [ ] Personalized recommendations are displayed
- [ ] Docker containers start and communicate properly
- [ ] Application is responsive and user-friendly
