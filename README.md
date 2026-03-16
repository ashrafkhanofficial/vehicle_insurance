# 🚗 Vehicle Insurance Prediction – End-to-End MLOps Project

An **industry-style Machine Learning project** implementing a complete **MLOps pipeline** for predicting whether a customer will purchase vehicle insurance.

The project demonstrates **data engineering, model training, deployment, and CI/CD automation** using modern production tools.

---

# 📌 Project Overview

This project simulates a **real-world production ML system** by implementing a complete pipeline including:

* Data ingestion from **MongoDB Atlas**
* Data validation using schema-based checks
* Data transformation and preprocessing
* Model training and evaluation
* Model versioning and storage in AWS S3
* Docker-based containerization
* Automated CI/CD using GitHub Actions
* Cloud deployment on AWS EC2

The goal is to follow **industry-standard MLOps architecture**.

---

# ⚙️ Tech Stack

**Programming**

* Python
* Pandas
* Scikit-learn

**Database**

* MongoDB Atlas

**Cloud Services (AWS)**

* S3 (Model Storage)
* ECR (Docker Image Registry)
* EC2 (Application Hosting)
* IAM (Access Management)

**DevOps / MLOps**

* Docker
* GitHub Actions
* Self Hosted Runner
* Environment Variables

**Backend**

* FastAPI
* Jinja Templates

---

# 🧠 ML Pipeline Flow

The project follows a **modular machine learning pipeline**:

Data Source (MongoDB)
↓
Data Ingestion
↓
Data Validation
↓
Data Transformation
↓
Model Training
↓
Model Evaluation
↓
Model Registry (AWS S3)
↓
Prediction Pipeline
↓
FastAPI Application
↓
Docker Container
↓
CI/CD Deployment

Each stage generates **artifacts** that are passed to the next stage.

---

# 📂 Project Structure

vehicle_insurance_project/

notebook/
 EDA and experimentation

src/

 components/
  data_ingestion
  data_validation
  data_transformation
  model_trainer

 configuration/
  MongoDB and AWS connections

 constants/
  global configuration variables

 entity/
  config and artifact classes

 utils/
  helper utilities

 exception/
  custom exception handling

 logger/
  logging configuration

 pipeline/
  training and prediction pipelines

static/
 frontend assets

templates/
 HTML templates

app.py
 FastAPI application

Dockerfile
 container configuration

requirements.txt
 project dependencies

setup.py
 local package configuration

.github/workflows/
 CI/CD pipeline configuration

---

# 📊 Data Source

The dataset is stored in **MongoDB Atlas**.

A **data access layer** retrieves records from MongoDB and converts them into a **Pandas DataFrame** for processing inside the pipeline.

This design simulates **real production data ingestion workflows**.

---

# 📦 Artifacts

Each pipeline stage produces **artifacts** such as:

* Raw dataset
* Validated dataset
* Transformed dataset
* Trained model
* Evaluation metrics

Artifacts allow **reproducibility, debugging, and traceability** in ML systems.

---

# 📋 Logging and Exception Handling

The project implements **custom logging and exception modules** to ensure:

* structured logs
* easier debugging
* production monitoring support

---

# ☁️ Model Registry

Trained models are stored in **AWS S3**.

The pipeline compares:

New Model
vs
Current Production Model

If the new model performs better, it replaces the existing model.

---

# 🐳 Docker Containerization

The application is packaged into a **Docker container** which includes:

* trained model
* prediction pipeline
* FastAPI server

This ensures **consistent environments across development and production**.

---

# 🔄 CI/CD Pipeline

Deployment is automated using **GitHub Actions**.

Pipeline flow:

Code Push (GitHub)
↓
Build Docker Image
↓
Push Image to AWS ECR
↓
Pull Image on EC2
↓
Run Docker Container
↓
Deploy Application

A **self-hosted runner on EC2** executes the deployment workflow.

---

# 🖥 Deployment Architecture

Developer
↓
GitHub Repository
↓
GitHub Actions (CI/CD)
↓
Docker Image Build
↓
AWS ECR
↓
EC2 Self Hosted Runner
↓
Docker Container
↓
FastAPI Application

---

# 🌐 Application Interface

The project provides a **web interface** where users can:

* enter customer and vehicle details
* send prediction requests
* receive insurance purchase predictions

The API backend is implemented using **FastAPI**.

---

# 🚀 Running the Project

Clone repository

git clone <repository-url>
cd vehicle_insurance_project

Create environment

conda create -n vehicle python=3.10
conda activate vehicle

Install dependencies

pip install -r requirements.txt

Run application

python app.py

---

# 📈 Key Learning Outcomes

This project demonstrates:

* End-to-End ML Pipeline Development
* Data Engineering for Machine Learning
* Modular ML Architecture
* Model Versioning
* Containerized ML Deployment
* CI/CD Automation for ML Systems
* Cloud Deployment with AWS

---

# 📬 Author

Vehicle Insurance Prediction – MLOps Project

Built to demonstrate **industry-grade machine learning system design and deployment practices**.
