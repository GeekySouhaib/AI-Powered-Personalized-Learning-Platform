# AI-Powered Personalized Learning Platform

This project is a full-stack application that provides an interactive learning platform with AI-powered personalization features. The platform allows users to register, browse courses, access lessons, and receive personalized recommendations based on their learning patterns.

## Features

- User authentication (register/login)
- Course browsing and filtering
- Lesson viewing with progress tracking
- AI-powered learning assistant for answering questions
- Personalized course and resource recommendations
- Responsive design for all devices

## Tech Stack

- **Frontend**: React, Material UI, React Router
- **Backend**: Node.js, Express, Sequelize
- **Database**: SQLite (for simplicity, can be replaced with PostgreSQL in production)
- **Containerization**: Docker, Docker Compose

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Docker and Docker Compose (for containerized deployment)

### Running Locally

#### Backend Setup

1. Navigate to the backend directory:
   ```
   cd learning_platform/backend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the development server:
   ```
   npm run dev
   ```

The backend server will run on http://localhost:5000.

#### Frontend Setup

1. Navigate to the frontend directory:
   ```
   cd learning_platform/frontend
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the development server:
   ```
   npm start
   ```

The frontend application will run on http://localhost:3000.

### Running with Docker

For a containerized deployment that includes both frontend and backend:

1. From the project root directory:
   ```
   cd learning_platform
   ```

2. Build and start the containers:
   ```
   docker-compose up --build
   ```

3. Access the application:
   - Frontend: http://localhost
   - Backend API: http://localhost:5000

## Project Structure

```
learning_platform/
├── backend/                # Node.js Express backend
│   ├── config/             # Configuration files
│   ├── controllers/        # Request handlers
│   ├── models/             # Database models
│   ├── routes/             # API routes
│   ├── utils/              # Utility functions
│   ├── .env                # Environment variables
│   ├── Dockerfile          # Backend Docker configuration
│   └── server.js           # Entry point
├── frontend/               # React frontend
│   ├── public/             # Static files
│   ├── src/                # Source code
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   └── App.js          # Main component
│   ├── Dockerfile          # Frontend Docker configuration
│   └── package.json        # Dependencies
├── docker-compose.yml      # Docker Compose configuration
└── README.md               # Project documentation
```

## API Endpoints

### Authentication

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login with user credentials

### Courses

- `GET /api/courses` - Get all courses
- `GET /api/courses/:id` - Get a specific course with lessons
- `POST /api/courses` - Create a new course (requires authentication)

## AI Features

The platform includes two main AI-powered features:

1. **AI Learning Assistant**: A chatbot-like interface that helps users with questions about course content, provides explanations, and suggests resources.

2. **Personalized Recommendations**: A system that analyzes user learning patterns and suggests courses, resources, and concepts based on their progress and interests.

In this demonstration version, these features use simulated AI responses. In a production environment, they would be connected to actual AI services or models.

## Customization

### Environment Variables

Backend environment variables can be set in the `.env` file:

```
PORT=5000
JWT_SECRET=your_jwt_secret_key
```

Frontend environment variables can be set in the `.env` file in the frontend directory:

```
REACT_APP_API_URL=http://localhost:5000/api
```

## Future Enhancements

- Integration with real AI services for personalization
- User progress tracking and analytics
- Content creation tools for instructors
- Social learning features (discussions, peer reviews)
- Mobile application

## Troubleshooting

- If you encounter database issues, check that the SQLite file has proper permissions
- For Docker deployment issues, ensure ports 80 and 5000 are available on your machine
- If the frontend can't connect to the backend, verify the API URL in the frontend environment variables
