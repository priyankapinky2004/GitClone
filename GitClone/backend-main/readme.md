# Git Clone Project Backend

This repository contains the backend server code for the Git Clone project, which interacts with Git repositories, handles various Git operations, and serves the necessary APIs for front-end consumption.

## Features

- **Clone Repositories:** Clone remote Git repositories to the local machine.
- **Pull Updates:** Pull the latest updates from remote repositories.
- **Push Changes:** Push local changes to the remote repository.
- **Create Repositories:** Create new Git repositories locally.
- **Commit Changes:** Commit local changes with custom messages.
- **Branch Management:** Create, delete, and manage branches.
- **User Authentication:** Secure API access with user authentication.
- **Logs & Errors:** Provides logs for successful and failed operations.

## Requirements

- **Node.js:** Version 14.x or above.
- **Git:** Git must be installed and accessible via the command line.
- **Database:** MongoDB or PostgreSQL (depending on the database used).
- **Environment:** Linux, macOS, or Windows (with WSL for Windows).

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/priyankapinky2004/GitClone.git
   cd git-clone-backend

Install dependencies:

npm install
Configure Environment Variables: Create a .env file at the root of the 

project and add the following variables:
GIT_PATH=/path/to/your/git/installation
DATABASE_URL=your_database_url
PORT=5000
JWT_SECRET=your_jwt_secret_key
Set up the database: If you are using MongoDB, ensure it’s running. For PostgreSQL, set up the connection string in .env.

Run the backend server:

npm run dev
The backend server should now be running on http://localhost:5000.

API Endpoints
POST /api/repository/clone
Description: Clone a remote repository to the local machine.

Request Body:

{
  "repoUrl": "https://github.com/user/repository.git",
  "destinationPath": "/path/to/clone/destination"
}
Response:

Status: 200 OK for success.

Error: 400 Bad Request if the repository URL or destination is invalid.

POST /api/repository/pull
Description: Pull the latest changes from the remote repository.

Request Body:

{
  "repoPath": "/path/to/repository"
}
Response:

Status: 200 OK for success.

Error: 400 Bad Request if the repository is not valid.

POST /api/repository/commit
Description: Commit changes in the local repository.

Request Body:

{
  "repoPath": "/path/to/repository",
  "commitMessage": "Fixing the bug in the API"
}
Response:

Status: 200 OK for success.

Error: 400 Bad Request if commit fails.

POST /api/user/authenticate
Description: Authenticate user for access to protected routes.

Request Body:

{
  "username": "user",
  "password": "password"
}
Response:

Status: 200 OK with JWT token.

Error: 401 Unauthorized for invalid credentials.

Running Tests
Run tests:

npm test
This will run the test suite for your backend using a testing framework like Mocha or Jest.

Contribution
Fork the repository.

Create your feature branch (git checkout -b feature/your-feature).

Commit your changes (git commit -am 'Add new feature').

Push to the branch (git push origin feature/your-feature).

Create a new Pull Request.

You can copy this and paste it directly into your `README.md` file. Let me know if you need further a