Snippet Saver is a full-stack web application that allows users to securely create, store, manage, and retrieve code snippets. It is designed to help developers organize reusable code efficiently.

This project is fully Dockerized, meaning the frontend, backend, and supporting services run inside containers using Docker Engine and Docker Compose, ensuring consistent setup across all systems without manual dependency installation.

🏗️ Tech Stack
🔹 Frontend

React / Vite

TypeScript

Nginx (for production build container)

🔹 Backend

Java (Spring Boot)

REST APIs

Authentication Service

🔹 DevOps

Docker

Docker Compose

🐳 Why Docker?

This project uses Docker to:

Eliminate “works on my machine” issues

Avoid installing Node, Java, or databases locally

Provide consistent runtime across all systems

Simplify deployment and testing

⚙️ Prerequisites

Before running the project, ensure you have:

✅ Docker installed

✅ Docker Engine running

Check installation:

docker --version
docker compose version
▶️ How to Run the Project (Using Docker Compose)
1️⃣ Clone the Repository
git clone https://github.com/YOUR_USERNAME/snippet-saver.git
cd snippet-saver
2️⃣ Build and Start Containers
docker compose up --build

This will:

Build backend image

Build frontend image

Start all required services

Connect containers via Docker network

3️⃣ Access the Application

After containers start successfully:

🌐 Open browser:

http://localhost:3000

(or the port defined in docker-compose.yml)

🛑 Stop the Application

To stop running containers:

docker compose down

To remove volumes as well:

docker compose down -v
📁 Project Structure
snippet-saver/
│
├── backend/
│   └── Spring Boot application
│
├── frontend/
│   └── React + Vite application
│
├── docker-compose.yml
└── README.md
🔐 Features

User Authentication

Create & Save Code Snippets

View and Manage Snippets

RESTful API Architecture

Containerized Deployment

🧪 Development Mode (Optional)

If running without Docker:

Backend:
cd backend
./mvnw spring-boot:run
Frontend:
cd frontend
npm install
npm run dev

(Docker is recommended for full project setup.)

📈 Future Improvements

Snippet tagging system

Search and filtering

Dark mode UI

Cloud deployment (AWS / Azure)

CI/CD integration
