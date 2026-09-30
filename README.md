# Tech Challenge 1 — CI/CD Pipeline

## Project Overview

This project demonstrates a complete CI/CD workflow using:

- GitHub
- GitHub Actions
- Docker
- Amazon ECR
- Amazon ECS Fargate
- Terraform
- Python Flask

The application is a simple Flask web application that returns:

```text
Hello from CI/CD Pipeline!


## Architecture

Developer
    |
    v
GitHub
    |
    v
GitHub Actions
    |
    +---- Build Docker Image
    |
    +---- Push Image to Amazon ECR
    |
    v
Amazon ECS Fargate
    |
    v
Running Flask Application

Terraform is used to provision the required AWS infrastructure.


## Project Structure

tech-challenge-1/
├── app/
│   ├── app.py
│   └── requirements.txt
├── terraform/
├── .github/
│   └── workflows/
├── Dockerfile
├── .dockerignore
├── .gitignore
└── README.md


## Application

The application is built with Python Flask and listens on port 5000.

Expected response:

Hello from CI/CD Pipeline!


## Local Application Setup

Create and activate a Python virtual environment:

python3 -m venv .venv
source .venv/bin/activate

Install dependencies:

pip install -r app/requirements.txt

Run the application:

python app/app.py

Open:

http://localhost:5000


## Docker

Build the Docker image:

docker build -t tech-challenge-1 .

Run the container:

docker run -d -p 5000:5000 --name tech-challenge-1-container tech-challenge-1

Open:

http://localhost:5000


## AWS Deployment

AWS infrastructure is provisioned using Terraform.

The CI/CD workflow will:

Build the Docker image.
Authenticate to Amazon ECR.
Push the Docker image to ECR.
Deploy the application to Amazon ECS Fargate.


## CI/CD

GitHub Actions is used to automate the deployment process whenever changes are pushed to the repository.

Technologies
Technology	    Purpose
Python Flask	    Web application
Docker	            Containerization
GitHub	            Source control
GitHub Actions	    CI/CD automation
Amazon ECR	    Container image registry
Amazon ECS Fargate  Container deployment
Terraform	    Infrastructure as Code
