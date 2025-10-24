# 🧠 Docker Model Runner

## 📘 Overview

A **Docker Model Runner** is a containerized environment designed to
**run or serve machine learning models**. It encapsulates the model,
dependencies, and runtime in a Docker container, making it portable,
scalable, and reproducible across environments.

Docker Model Runner (DMR) lets you run and manage AI models locally using Docker.

---

## ⚙️ Why Use a Docker Model Runner?

  -----------------------------------------------------------------------
  Reason                    Description
  ------------------------- ---------------------------------------------
  🧩 **Reproducibility**    Ensures the model runs consistently across
                            different machines and platforms.

  🚀 **Easy Deployment**    Can be deployed anywhere Docker runs---local,
                            cloud, or Kubernetes.

  🔒 **Isolation**          Keeps dependencies contained within the
                            container, preventing conflicts.

  🔁 **Scalability**        Easy to replicate containers to scale
                            inference workloads.

  🧠 **Model Serving**      Exposes models as REST/gRPC APIs for
                            real-time predictions.
  -----------------------------------------------------------------------
---

## 🛠️ How It's Used

### 1️⃣ **Custom-Built Model Runner**

- You can create your own model runner using Python frameworks like
**FastAPI** or **Flask**.
- You have a trained model (e.g., a .pkl, .onnx, or .pt file). Create a Docker container that loads the model, exposes an API endpoint, returns predictions when data is sent.   

### 2️⃣ **Framework-Based Model Runners**

You can also use established tools for model serving:

  ------------------------------------------------------------------------
  Tool           Description                       Use Case
  -------------- --------------------------------- -----------------------
  🧩 **NVIDIA    High-performance inference for    Enterprise GPU serving
  Triton         TensorFlow, PyTorch, ONNX, etc.   
  Inference                                        
  Server**                                         

  📦 **BentoML** Packages and containerizes models MLOps / Data Science
                 easily                            teams

  🔁 **MLflow    Versioned model packaging         Experiment tracking and
  Models**                                         reproducibility

  ☁️ **Seldon    Kubernetes-native model serving   Cloud-native MLOps
  Core /                                           
  KServe**                                         
  ------------------------------------------------------------------------

Example (BentoML):

``` bash
bentoml build
bentoml containerize service:latest
docker run -p 3000:3000 service:latest
```

---

## 👷 Hands on

# hello-genai - Docker

A simple chatbot web application built in Go, Python and Node.js that connects to a local LLM service (llama.cpp) to provide AI-powered responses.

## Quick Start

1. Clone the repository:
   ```bash
   git clone https://github.com/docker/hello-genai
   cd hello-genai
   ```

2. Start the application using Docker Compose:
   ```bash
   docker compose up
   ```
3. Open your browser and visit the following links:

   http://localhost:8080 for the GenAI Application in Go

   http://localhost:8081 for the GenAI Application in Python

   http://localhost:8082 for the GenAI Application in Node

   http://localhost:8083 for the GenAI Application in Rust

## Requirements

- macOS (recent version)
- Either:
  - Docker and Docker Compose (preferred)
  - Go 1.21 or later
- Local LLM server

---

## 📚 Resources

- 📘 [Docker Model Runner - DMR](https://docs.docker.com/ai/model-runner/get-started/)
- 📘 [DMR Examples](https://docs.docker.com/ai/model-runner/examples/)

## Sample Outputs
- 📸 [Sample model runner - smollm2](./docker-model-runner-smollm2.png)
- 📸 [hello-genai](./docker-model-runner-chatbot.png)
---
