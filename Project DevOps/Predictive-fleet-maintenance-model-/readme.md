---

# Predictive Fleet Maintenance System with Automated CI/CD Pipeline Integration

## Overview

This project combines **Machine Learning** and **DevOps** to create a production-ready Predictive Fleet Maintenance System.

The Machine Learning component predicts vehicle maintenance requirements using historical fleet data, while the DevOps component automates application packaging, validation, deployment, and delivery through a complete CI/CD pipeline.

The project demonstrates how an ML application can be transformed into a deployable and maintainable software system using industry-standard DevOps practices.

---

## Project Objectives

* Predict vehicle maintenance requirements using Machine Learning
* Containerize the application using Docker
* Implement Continuous Integration (CI) using GitHub Actions
* Implement Continuous Deployment (CD) using Jenkins
* Automate application validation and deployment
* Ensure environment consistency across deployments
* Demonstrate a complete end-to-end DevOps workflow

---

# System Architecture

```text
                     +----------------+
                     |     User       |
                     +--------+-------+
                              |
                              v
                    +-------------------+
                    | Streamlit Frontend|
                    +--------+----------+
                             |
                             v
                    +-------------------+
                    | ML Prediction     |
                    | Engine            |
                    +--------+----------+
                             |
                             v
                    +-------------------+
                    | Trained Model     |
                    | (model.pkl)       |
                    +-------------------+

                             |
                             v

                    +-------------------+
                    | Docker Container  |
                    +--------+----------+
                             |
                             v
                    +-------------------+
                    | GitHub Repository |
                    +--------+----------+
                             |
                             v
                    +-------------------+
                    | GitHub Actions CI |
                    +--------+----------+
                             |
                             v
                    +-------------------+
                    | Jenkins CD        |
                    +--------+----------+
                             |
                             v
                    +-------------------+
                    | Live Deployment   |
                    +-------------------+
```

---

# Machine Learning Component

## Problem Statement

Fleet vehicles generate large volumes of operational and maintenance data. Unexpected failures increase operational costs and vehicle downtime.

This project uses Machine Learning to predict maintenance requirements before failures occur.

---

## ML Workflow

```text
Fleet Dataset
      |
      v
Data Preprocessing
      |
      v
Feature Engineering
      |
      v
Model Training
      |
      v
Model Evaluation
      |
      v
Saved Model (model.pkl)
      |
      v
Streamlit Prediction Interface
```

---

## Dataset

The dataset contains fleet-related vehicle information such as:

* Vehicle Age
* Mileage
* Engine Parameters
* Maintenance History
* Usage Metrics

These features are used to generate maintenance predictions.

---

## Model Artifacts

```text
model/
│
├── model.pkl
├── scaler.pkl
└── columns.json
```

### model.pkl

Stores the trained machine learning model.

### scaler.pkl

Stores the feature scaling object used during training.

### columns.json

Stores feature column information required during inference.

---

## User Workflow

```text
User Inputs Vehicle Data
            |
            v
Preprocessing
            |
            v
Feature Scaling
            |
            v
Model Prediction
            |
            v
Maintenance Result Displayed
```

---

# DevOps Implementation

The original ML application was transformed into a deployment-ready system using modern DevOps practices.

---

## DevOps Objectives

* Containerization
* Deployment Automation
* Continuous Integration
* Continuous Deployment
* Environment Consistency
* Infrastructure Automation

---

# Docker Containerization

Docker packages the application and its dependencies into a portable container.

## Docker Workflow

```text
Create Dockerfile
        |
        v
Build Docker Image
        |
        v
Run Docker Container
        |
        v
Access Application
(localhost:8501)
```

---

## Docker Commands

### Build Image

```bash
docker build -f devops/Dockerfile -t fleet-maintenance-app .
```

### Run Container

```bash
docker run -d -p 8501:8501 --name fleet-container fleet-maintenance-app
```

### Verify Running Container

```bash
docker ps
```

---

# Continuous Integration (CI)

Implemented using GitHub Actions.

Every push automatically triggers validation and build processes.

## CI Workflow

```text
Developer Pushes Code
          |
          v
GitHub Actions Triggered
          |
          v
Install Dependencies
          |
          v
Validate Environment
          |
          v
Build Docker Image
          |
          v
CI Success
```

---

# Continuous Deployment (CD)

Implemented using Jenkins.

After successful validation, Jenkins automatically deploys the latest version.

## CD Workflow

```text
Jenkins Pulls Latest Code
            |
            v
Build Docker Image
            |
            v
Stop Existing Container
            |
            v
Deploy Updated Container
            |
            v
Application Available
```

---

# Integrated CI/CD Pipeline

```text
Developer Push
       |
       v
GitHub Repository
       |
       v
GitHub Actions CI
       |
       v
Dependency Validation
       |
       v
Docker Build Validation
       |
       v
Jenkins CD
       |
       v
Container Deployment
       |
       v
Live Application
```

---

# Project Structure

```text
Predictive-Fleet-Maintenance/
│
├── frontend/
│   └── app.py
│
├── backend/
│
├── model/
│   ├── model.pkl
│   ├── scaler.pkl
│   └── columns.json
│
├── dataset/
│   └── fleet_data.csv
│
├── devops/
│   ├── Dockerfile
│   └── Jenkinsfile
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── screenshots/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# Technologies Used

## Machine Learning

* Python
* Pandas
* NumPy
* Scikit-learn
* Joblib

## Frontend

* Streamlit

## DevOps

* Docker
* Git
* GitHub
* GitHub Actions
* Jenkins

---

# Application Access

## Local Deployment

```text
http://localhost:8501
```

## Jenkins Dashboard

```text
http://localhost:8080
```

---

# Key Features

### Machine Learning

* Predictive maintenance analysis
* Feature preprocessing
* Scaled model inference
* Interactive prediction interface

### DevOps

* Docker containerization
* Automated CI pipeline
* Automated CD pipeline
* Docker-based deployment
* Jenkins automation
* GitHub Actions integration

---

# Results

Successfully implemented:

* End-to-End ML Application Deployment
* Docker Containerization
* Continuous Integration
* Continuous Deployment
* Automated Build Validation
* Automated Container Deployment
* Deployment Consistency Across Environments

---

# Future Enhancements

* Kubernetes Deployment
* Docker Compose Support
* Cloud Deployment (AWS/Azure/GCP)
* Automated Unit Testing
* Monitoring with Prometheus
* Visualization with Grafana
* Model Retraining Pipeline
* MLOps Integration

---

# Learning Outcomes

Through this project, the following concepts were implemented and understood:

* Machine Learning Deployment
* Docker Containerization
* Continuous Integration (CI)
* Continuous Deployment (CD)
* GitHub Actions Workflows
* Jenkins Pipelines
* DevOps Automation
* Infrastructure Consistency
* Automated Software Delivery

---

# Author

**Abhiram Bency**
B.Tech Computer Science Engineering

---

## Repository Highlights

⭐ Machine Learning Application
⭐ Docker Containerization
⭐ GitHub Actions CI
⭐ Jenkins CD
⭐ Automated CI/CD Pipeline
⭐ Deployment Automation
⭐ Production-Oriented DevOps Workflow

This README is strong enough for:

* GitHub portfolio projects
* internship applications
* ML/AI roles
* DevOps roles
* academic project submissions
* resume project links
