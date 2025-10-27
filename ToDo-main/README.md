# Todo Application

A full-stack Todo application built with React and Node.js, featuring user authentication and personalized task management.

## Features

### 🔐 Authentication System
- **User Registration**: Create new accounts with unique usernames
- **Secure Login**: JWT-based authentication with password hashing
- **Session Management**: Persistent login sessions with token verification
- **Protected Routes**: Dashboard access only for authenticated users

### ✅ Todo Management
- **Personal Todos**: Each user sees only their own tasks
- **CRUD Operations**: Create, Read, Update, and Delete todos
- **Status Tracking**: Mark todos as pending or completed
- **Real-time Updates**: Instant UI updates for all operations
- **Task Statistics**: View total, pending, and completed task counts

### 🎨 Modern UI/UX
- **Responsive Design**: Works seamlessly on all device sizes
- **Glassmorphism Effects**: Modern transparent card designs
- **Smooth Animations**: Hover effects and transitions
- **Clean Interface**: Intuitive and user-friendly design

## Technology Stack

### Backend (Node.js)
- **Express.js**: Web application framework
- **JWT**: JSON Web Tokens for authentication
- **bcryptjs**: Password hashing and encryption
- **UUID**: Unique identifier generation
- **CORS**: Cross-origin resource sharing
- **JSON File Storage**: Simple file-based data persistence

### Frontend (React)
- **React 18**: Modern React with hooks
- **React Router DOM**: Client-side routing
- **Axios**: HTTP client for API requests
- **Context API**: State management for authentication
- **CSS3**: Modern styling with gradients and animations

## Project Structure

```
TodoApp/
├── backend/
│   ├── server.js          # Express server with all API endpoints
│   ├── package.json       # Backend dependencies
│   ├── users.json         # User data storage
│   └── todos.json         # Todo data storage
└── frontend/
    ├── src/
    │   ├── components/
    │   │   └── ProtectedRoute.js
    │   ├── context/
    │   │   └── AuthContext.js
    │   ├── pages/
    │   │   ├── Login.js
    │   │   ├── Signup.js
    │   │   ├── Dashboard.js
    │   │   ├── Auth.css
    │   │   └── Dashboard.css
    │   ├── services/
    │   │   └── api.js
    │   ├── App.js
    │   └── App.css
    └── package.json
```

## API Endpoints

### Authentication
- `POST /api/signup` - Register new user
- `POST /api/login` - User login
- `GET /api/verify` - Verify JWT token

### Todos
- `GET /api/todos` - Get user's todos
- `POST /api/todos` - Create new todo
- `PUT /api/todos/:id` - Update todo
- `DELETE /api/todos/:id` - Delete todo

## Data Models

### User Model
```json
{
  "id": "unique-uuid",
  "username": "string",
  "password": "hashed-string",
  "createdAt": "ISO-date-string"
}
```

### Todo Model
```json
{
  "id": "unique-uuid",
  "userId": "user-uuid",
  "title": "string",
  "status": "pending|completed",
  "createdAt": "ISO-date-string",
  "updatedAt": "ISO-date-string"
}
```

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd TodoApp
   ```

2. **Install Backend Dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

### Running the Application

1. **Start the Backend Server** (Port 5000)
   ```bash
   cd backend
   npm start
   ```

2. **Start the Frontend Development Server** (Port 3000)
   ```bash
   cd frontend
   npm start
   ```

3. **Access the Application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000/api

## Usage

1. **Sign Up**: Create a new account with a unique username
2. **Sign In**: Log in with your credentials
3. **Add Todos**: Use the input field to create new tasks
4. **Manage Todos**: 
   - Check/uncheck to mark as complete/pending
   - Click edit (✏️) to modify task titles
   - Click delete (🗑️) to remove tasks
5. **View Statistics**: See your task counts in the dashboard
6. **Logout**: Use the logout button to end your session

## Security Features

- **Password Hashing**: All passwords are hashed using bcrypt
- **JWT Authentication**: Secure token-based authentication
- **Protected Routes**: API endpoints require valid tokens
- **User Isolation**: Users can only access their own data
- **Input Validation**: Server-side validation for all inputs

## Future Enhancements

- [ ] Due dates for todos
- [ ] Priority levels (high, medium, low)
- [ ] Categories/tags for todos
- [ ] Search and filter functionality
- [ ] Email verification
- [ ] Password reset functionality
- [ ] Database integration (MongoDB/PostgreSQL)
- [ ] File attachments for todos
- [ ] Real-time updates with WebSocket

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License.

---

**Developed with ❤️ using React and Node.js**
