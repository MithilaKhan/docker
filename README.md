# 🐳 Dockerized Next.js App

This project is a Next.js application that has been fully containerized using Docker, making it easy to run consistently across different environments without worrying about local dependencies.

## 🚀 Getting Started with Docker

You do not need to have Node.js installed locally to run this project. All you need is **Docker** and **Docker Compose**.

### 1. Build and Run the Container

From the root of the project, run the following command to build the Docker image and start the container in detached mode:

```bash
docker-compose up --build -d
```

### 2. Access the Application

Once the container is running, the application will be accessible at:

- **http://localhost:3000** (Primary Port)
- **http://localhost:3001** (Mapped Port)

### 3. Stopping the Container

To stop the running application, execute:

```bash
docker-compose down
```

---

## 🛠️ How It Works

- **`Dockerfile`**: Defines the Node.js environment, installs dependencies via `npm install`, and runs the application using `npm start`.
- **`docker-compose.yml`**: Orchestrates the Docker container, maps ports (`3000` and `3001`), and sets up volume binding so that your local changes reflect inside the container. It also creates an anonymous volume for `node_modules` to prevent local modules from overwriting the container's modules.
