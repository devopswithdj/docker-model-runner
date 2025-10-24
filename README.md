# 🧠 Docker Model Runner

## 📘 Overview
A **Docker Model Runner** is a containerized environment designed to run or serve machine learning models. It encapsulates the model, dependencies, and runtime in a Docker container, making it portable, scalable, and reproducible across environments.

Docker Model Runner (DMR) lets you run and manage AI models locally using Docker.

## ⚙️ Why Use a Docker Model Runner?

| Reason | Description |
|--------|-------------|
| 🧩 **Reproducibility** | Ensures the model runs consistently across different machines and platforms |
| 🚀 **Easy Deployment** | Can be deployed anywhere Docker runs---local, cloud, or Kubernetes |
| 🔒 **Isolation** | Keeps dependencies contained within the container, preventing conflicts |
| 🔁 **Scalability** | Easy to replicate containers to scale inference workloads |
| 🧠 **Model Serving** | Exposes models as REST/gRPC APIs for real-time predictions |

## 🛠️ How It's Used

### 1️⃣ Custom-Built Model Runner
- Create your own model runner using Python frameworks like **FastAPI** or **Flask**
- Package trained models (.pkl, .onnx, .pt) in Docker containers
- Expose API endpoints for model inference

### 2️⃣ Framework-Based Model Runners

| Tool | Description | Use Case |
|------|-------------|----------|
| 🧩 **NVIDIA Triton** | High-performance inference for TensorFlow, PyTorch, ONNX | Enterprise GPU inference |
| 📦 **BentoML** | Python framework for model containerization | ML pipeline deployment |
| 🔁 **MLflow Models** | Automatic Docker image packaging | Model versioning |
| ☁️ **Seldon Core/KServe** | Kubernetes-native serving | MLOps environments |

**Example (BentoML):**
```bash
bentoml build
bentoml containerize service:latest
docker run -p 3000:3000 service:latest
```

## 👷 Hands-on: Hello GenAI

A simple chatbot web application using Go, Python, Node.js and Rust that connects to a local LLM service (llama.cpp).

### Quick Start

1. Clone the repository:
```bash
git clone https://github.com/docker/hello-genai
cd hello-genai
```

2. Start with Docker Compose:
```bash
docker compose up
```

3. Access the applications:
- Go version: http://localhost:8080
- Python version: http://localhost:8081
- Node.js version: http://localhost:8082
- Rust version: http://localhost:8083

### Requirements
- Operating System: macOS (recent version)
- Tools (one of):
  - Docker and Docker Compose (recommended)
  - Go 1.21+
- Local LLM server

## 📚 Resources
- [Docker Model Runner Documentation](https://docs.docker.com/ai/model-runner/get-started/)
- [DMR Examples](https://docs.docker.com/ai/model-runner/examples/)

## 📸 Screenshots
- [Model Runner Demo (smollm2)](./docker-model-runner-smollm2.png)
- [Hello GenAI Demo](./docker-model-runner-chatbot.png)