Here's an updated version of the README to include the DevOps implementation details:

---

# React-Node Recipe App 🍲

Welcome to the React-Node Recipe App! This application allows users to view, add, and manage their favorite recipes. It's built using React for the frontend and Node.js with Prisma for the backend.

## Getting Started 🚀

### Prerequisites:

- Node.js and npm installed on your machine.
- An account on [ElephantSQL](https://www.elephantsql.com/) for the database.
- A [Spoonacular API key](https://spoonacular.com/food-api) for the recipe API.

### Setting Up:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/chrisblakely01/react-node-recipe-app.git
   cd react-node-recipe-app
   ```

2. **Setting up the Backend**:

   - Navigate to the backend directory:
     ```bash
     cd backend
     ```

   - Install the necessary packages:
     ```bash
     npm install
     ```

   - **Spoonacular API**:
     - Add the API key to the `API_KEY` variable in the `.env` file.   

   - **ElephantSQL Setup**:
     - Create a new database instance on ElephantSQL.
     - Copy the connection string provided by ElephantSQL.

   - **Prisma Setup**:
     - Replace the `DATABASE_URL` in the `.env` file with your ElephantSQL connection string.
     - Initialize Prisma and generate the Prisma client:
       ```bash
       npx prisma init
       npx prisma generate
       ```

   - Start the backend server:
     ```bash
     npm start
     ```

3. **Setting up the Frontend**:

   - Navigate to the frontend directory:
     ```bash
     cd frontend
     ```

   - Install the necessary packages:
     ```bash
     npm install
     ```

   - Start the frontend development server:
     ```bash
     npm run dev
     ```

## DevOps Implementation 🌐

### Infrastructure Setup:

- **EC2 Instance**: Created an EC2 instance on AWS (t2.medium) to support the app architecture after testing with t2.micro and t2.small.
- **SSH Access**: Secured login to the server via SSH.

### Jenkins and Docker Setup:

1. **Jenkins Installation**:
   - Installed Jenkins using AWS CLI.
   - Configured Jenkins for managing CI/CD pipelines.

2. **Docker Installation**:
   - Installed Docker on the EC2 instance.
   - Granted necessary permissions to Jenkins for executing Docker commands.

### CI/CD Pipeline:

1. **Code Cloning**:
   - Cloned the repository from GitHub.

2. **Building and Testing**:
   - Wrote a Dockerfile and created Docker images for the application.
   - Built and tested the application using Docker.

3. **Docker Hub Integration**:
   - Pushed the Docker images to Docker Hub securely using environment variables.

4. **Deployment**:
   - Used Docker Compose to create and manage containers for the application.
   - Deployed the application to the AWS EC2 instance.

This setup ensures efficient, automated deployment and management of the React-Node Recipe App.

---
