# Multi-Agent AI Tutoring System - Setup Guide

This guide will help you set up and run the Multi-Agent AI Tutoring System on your local machine.

## Prerequisites

- Python 3.8 or higher
- Node.js 16 or higher
- npm or yarn
- Google Gemini API key (for AI functionality)
- Git

## Quick Start

### 1. Clone the Repository

```bash
git clone <repository-url>
cd TUTOR_AI
```

### 2. Backend Setup

#### Install Python Dependencies

```bash
cd backend
python -m venv venv

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate

pip install -r requirements.txt
```

#### Configure Environment Variables

```bash
# Copy the example environment file
cp env.example .env

# Edit .env file with your configuration
# Most importantly, add your GEMINI_API_KEY
```

#### Initialize Database

```bash
# The database will be automatically created when you run the application
# No additional setup required for SQLite
```

#### Run the Backend

```bash
python main.py
```

The backend will be available at `http://localhost:8000`

### 3. Frontend Setup

#### Install Node.js Dependencies

```bash
cd frontend
npm install
```

#### Configure Environment Variables

```bash
# Copy the example environment file
cp env.example .env

# Edit .env file if needed (usually default values work)
```

#### Run the Frontend

```bash
npm run dev
```

The frontend will be available at `http://localhost:3000`

## Configuration

### Backend Configuration (.env)

Key configuration options:

```env
# AI/LLM settings
GEMINI_API_KEY=your_gemini_api_key_here

# Security
SECRET_KEY=your-super-secret-key-change-this-in-production

# Database
DATABASE_URL=sqlite:///./tutoring_system.db

# CORS (for frontend communication)
ALLOWED_HOSTS=["http://localhost:3000", "http://localhost:5173"]
```

### Frontend Configuration (.env)

```env
VITE_API_BASE_URL=http://localhost:8000/api/v1
```

## API Documentation

Once the backend is running, you can access the interactive API documentation at:

- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## System Architecture

### Backend Components

1. **FastAPI Application** (`main.py`)
   - Main application entry point
   - Middleware configuration
   - Route registration

2. **AI Agents** (`app/agents/`)
   - Content Generator Agent
   - Question Setter Agent
   - Feedback Evaluator Agent

3. **Database Models** (`app/models/`)
   - User management
   - Session tracking
   - Content storage
   - Question management
   - Feedback system

4. **API Endpoints** (`app/api/v1/endpoints/`)
   - Authentication
   - User management
   - Session management
   - Content generation
   - Question generation
   - Feedback evaluation

5. **Core Services** (`app/core/`)
   - Configuration management
   - Database connection
   - Security utilities
   - Logging system

### Frontend Components

1. **React Application** (`src/`)
   - Modern React with TypeScript
   - Vite for fast development
   - TailwindCSS for styling

2. **Context Providers** (`src/contexts/`)
   - Authentication context
   - Theme context

3. **Components** (`src/components/`)
   - Layout components
   - Navigation
   - Protected routes

4. **Pages** (`src/pages/`)
   - Home page
   - Dashboard
   - Authentication pages
   - Feature pages (placeholder)

## Features

### ✅ Implemented

- **Multi-Agent AI System**
  - Content Generator Agent
  - Question Setter Agent
  - Feedback Evaluator Agent
  - Inter-agent communication

- **Security Features**
  - JWT authentication
  - Password hashing
  - Input sanitization
  - Role-based access control

- **Database Management**
  - SQLite database (default)
  - SQLAlchemy ORM
  - Comprehensive data models

- **API System**
  - RESTful API endpoints
  - OpenAPI documentation
  - Error handling
  - Request validation

- **Frontend Interface**
  - Modern React application
  - Dark/Light theme support
  - Responsive design
  - Authentication flow

### 🚧 In Development

- **Advanced Features**
  - Real-time chat interface
  - File upload system
  - Advanced analytics
  - Email notifications

- **Enhanced AI Capabilities**
  - Multi-modal content generation
  - Advanced question types
  - Personalized learning paths

## Testing

### Backend Testing

```bash
cd backend
pytest
```

### Frontend Testing

```bash
cd frontend
npm test
```

## Deployment

### Backend Deployment

1. **Production Environment**
   ```bash
   # Set DEBUG=False in .env
   # Use PostgreSQL instead of SQLite
   # Configure proper CORS settings
   ```

2. **Using Docker**
   ```bash
   docker build -t tutoring-ai-backend .
   docker run -p 8000:8000 tutoring-ai-backend
   ```

### Frontend Deployment

1. **Build for Production**
   ```bash
   cd frontend
   npm run build
   ```

2. **Deploy to Static Hosting**
   - Netlify
   - Vercel
   - AWS S3
   - GitHub Pages

## Troubleshooting

### Common Issues

1. **Database Connection Error**
   - Ensure SQLite file is writable
   - Check DATABASE_URL in .env

2. **AI Agent Errors**
   - Verify GEMINI_API_KEY is set
   - Check API key permissions
   - Ensure internet connection

3. **CORS Errors**
   - Verify ALLOWED_HOSTS in backend .env
   - Check frontend API_BASE_URL

4. **Authentication Issues**
   - Clear browser storage
   - Check JWT token expiration
   - Verify SECRET_KEY is set

### Logs

- Backend logs: `backend/logs/`
- Frontend logs: Browser console
- API logs: Backend console output

## Support

For issues and questions:

1. Check the troubleshooting section
2. Review API documentation at `/docs`
3. Check logs for error details
4. Create an issue in the repository

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## License

This project is licensed under the MIT License.
