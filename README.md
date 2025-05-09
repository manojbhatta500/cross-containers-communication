# Full Stack Docker Project

This project is a practical implementation of Docker concepts in a full-stack application, demonstrating container networking, data persistence, and development workflows. It consists of three separate containers:
- MongoDB container (separate database container)
- Node.js backend container (communicates with MongoDB)
- React frontend container (communicates with backend)

## Project Structure

```
fullstackdocker/
├── backend/         # Node.js backend with MongoDB
├── frontend/        # React frontend
└── README.md
```

## Key Docker Concepts Learned

### 1. Container Communication
- Three separate containers communicating through Docker's internal network
  - MongoDB container: Database storage
  - Backend container: Business logic and API endpoints
  - Frontend container: User interface
- Clear separation of concerns between containers
- Communication flow: Frontend ↔ Backend ↔ MongoDB

### 2. Data Persistence
#### MongoDB
- Implemented data persistence using Docker volumes
- Ensures data remains even after container restarts
- Limited access through proper network configuration

#### Backend
- Persistent logging through Docker volumes
- Logs directory mounted to host machine
- Environment variables for configuration

#### Frontend
- Live source code updates using Docker volumes
- Development environment setup for hot reloading

### 3. Environment Configuration
- Utilized environment variables in Dockerfiles
- Configurable settings through `.env` files
- Example:
  ```
  ENV USERNAME=user
  ENV PASSKEY=secret
  ```

### 4. Docker Best Practices
- Implemented `.dockerignore` files in all directories
- Optimized Dockerfile layers for better caching
- Proper port exposure and container networking
- Separation of concerns between containers

## Implementation Details

### Backend Container
- Node.js application with MongoDB connectivity
- Persistent logging through mounted volumes
- Environment variable configuration
- Live code updates during development

### Frontend Container
- React application with hot reloading
- Development environment setup
- Communication with backend container
- Volume mounting for source code changes

### MongoDB Container
- Persistent data storage
- Limited access through mongodb authentication configuration
- Containerized database deployment

## Learning Outcomes

1. **Container Networking**
   - How containers communicate in a Docker network
   - Setting up proper network configurations
   - Inter-container communication patterns

2. **Data Persistence**
   - Different types of Docker volumes
   - Implementation of persistent storage
   - Best practices for data management

3. **Development Workflow**
   - Live code updates in containers
   - Development environment setup
   - Debugging techniques

4. **Security**
   - Environment variable usage
   - Limited container access
   - Proper network isolation

This project serves as a practical example of implementing Docker concepts in a full-stack application, demonstrating how to properly manage container communication, data persistence, and development workflows.