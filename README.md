# Node Todo CI/CD

A simple and containerized Todo application built with Node.js and Express, with DevOps tooling for containerization, testing, code quality, and Kubernetes deployment.

## 🚀 Project Overview

This project demonstrates how a Node.js Todo application can be packaged and prepared for a modern DevOps workflow.

The application includes:

- Node.js
- Express.js
- EJS
- Docker
- Docker Compose
- Kubernetes
- Kustomize
- SonarQube configuration
- Automated testing

The main goal of this project is to practice deploying and managing a web application using DevOps tools and technologies.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Node.js | Application runtime |
| Express.js | Backend web framework |
| EJS | Server-side HTML rendering |
| Docker | Containerization |
| Docker Compose | Multi-container/local orchestration |
| Kubernetes | Container orchestration |
| Kustomize | Kubernetes configuration management |
| SonarQube | Code quality analysis |
| JavaScript | Application development |
| npm | Package management |

## 📁 Project Structure

```text
node-todo-cicd/
│
├── views/                  # EJS frontend views
│   ├── todo.ejs
│   └── edititem.ejs
│
├── k8s/                    # Kubernetes manifests
│
├── kustomize/              # Kustomize configuration
│
├── app.js                  # Main application
├── test.js                 # Application tests
├── package.json            # Project dependencies and scripts
├── package-lock.json       # Dependency lock file
│
├── Dockerfile              # Docker image configuration
├── docker-compose.yaml     # Docker Compose configuration
│
├── sonar-project.properties # SonarQube configuration
├── .gitignore
└── README.md
```

## 💻 Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/node-todo-cicd.git
cd node-todo-cicd
```

### 2. Install dependencies

```bash
npm install
```

### 3. Start the application

```bash
node app.js
```

The application will be available on the port configured by the application.

## 🐳 Run with Docker

Build the Docker image:

```bash
docker build -t node-todo-cicd .
```

Run the container:

```bash
docker run -d -p 3000:3000 --name node-todo node-todo-cicd
```

Then access:

```text
http://localhost:3000
```

> Change the port mapping if your application uses a different port.

## 🐳 Run with Docker Compose

Start the application using Docker Compose:

```bash
docker compose up -d
```

Check running containers:

```bash
docker compose ps
```

View logs:

```bash
docker compose logs -f
```

Stop the application:

```bash
docker compose down
```

## ☸️ Kubernetes Deployment

Kubernetes manifests for the application are available in the `k8s` directory.

Example commands:

```bash
kubectl apply -f k8s/
```

Check the deployed resources:

```bash
kubectl get pods
kubectl get deployments
kubectl get services
```

## 🧩 Kustomize

Kustomize configuration is available in the `kustomize` directory.

Apply the configuration using:

```bash
kubectl apply -k kustomize/
```

To preview the generated Kubernetes resources:

```bash
kubectl kustomize kustomize/
```

## 🧪 Testing

Run the project tests using the npm script configured in `package.json`.

For example:

```bash
npm test
```

## 🔍 Code Quality

The project contains a `sonar-project.properties` file for SonarQube analysis.

A typical SonarQube workflow can include:

```text
Application
    ↓
Automated Tests
    ↓
SonarQube Code Analysis
    ↓
Docker Build
    ↓
Container Deployment
```

## 🔄 DevOps Workflow

The project is designed around the following workflow:

```text
Developer
    ↓
GitHub
    ↓
Testing
    ↓
SonarQube
    ↓
Docker Image
    ↓
Container Registry
    ↓
Kubernetes
    ↓
Application
```

## 🎯 Learning Objectives

This project was created to practice:

- Git and GitHub
- Node.js application deployment
- Docker containerization
- Docker Compose
- Kubernetes fundamentals
- Kustomize
- Testing
- SonarQube integration
- CI/CD concepts
- DevOps deployment workflow

## 📌 Future Improvements

Possible future improvements include:

- Jenkins CI/CD pipeline
- Docker image publishing to Docker Hub
- Kubernetes deployment automation
- Ingress configuration
- Monitoring and logging
- Security scanning
- Automated rollback
- Deployment to AWS

## 👨‍💻 Author

**Abhijeet Salunke**

Aspiring DevOps Engineer

GitHub: [abhijeet-salunke-in](https://github.com/abhijeet-salunke-in)

LinkedIn: [Abhijeet Salunke](https://www.linkedin.com/in/abhijeet-salunke-in/)

---

⭐ If you find this project useful, consider giving it a star.
