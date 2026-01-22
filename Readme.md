Java App 3.0 – CI/CD Enabled Java Application
📌 Project Overview

java_app_3_0 is a sample Java-based web application designed to demonstrate end-to-end DevOps practices using:

Maven for build automation

Jenkins for CI/CD pipelines

Docker for containerization

This project is mainly intended for DevOps interview preparation, hands-on practice, and CI/CD pipeline demonstrations.

🎯 Project Purpose

The main goals of this repository are:

Demonstrate how a Java application is built using Maven

Show how Jenkins automates build and deployment

Containerize the application using Docker

Serve as a base project for extending into Kubernetes, AWS, or advanced CI/CD workflows

This repo can be used as:

A DevOps practice project

A Jenkins pipeline demo

A Dockerized Java app example

🧱 Project Structure
java_app_3_0/
│── src/                     # Java source code
│   ├── main/java            # Application source
│   └── test/java            # (Can be added) Unit tests
│── pom.xml                  # Maven build configuration
│── Dockerfile               # Docker image instructions
│── Jenkinsfile              # Jenkins CI pipeline
│── README.md                # Project documentation
⚙️ Technologies Used

Java – Application development

Maven – Build & dependency management

Jenkins – Continuous Integration

Docker – Containerization

Git/GitHub – Version control

🚀 Application Build & Run
1️⃣ Build the Application (Maven)
mvn clean package

This command:

Downloads dependencies

Compiles source code

Generates a .jar file in the target/ directory

2️⃣ Run the Application Locally
java -jar target/*.jar
🐳 Docker Support
Build Docker Image
docker build -t java-app:3.0 .
Run Docker Container
docker run -d -p 8080:8080 java-app:3.0

Application will be available at:

http://localhost:8080
🔁 Jenkins CI/CD Pipeline

The Jenkinsfile automates the following stages:

Checkout Code from GitHub

Build Application using Maven

Docker Image Build

(Optional) Push image to Docker Hub / ECR

Jenkins Prerequisites

Jenkins installed

Maven configured in Jenkins

Docker installed on Jenkins server

GitHub webhook (optional for automation)

🧪 Future Enhancements (Recommended)

To make this project production-ready and similar to advanced DevOps repos:

✅ Add Maven Wrapper (mvnw, mvnw.cmd)

✅ Add Unit Tests under src/test/java

✅ Add Docker image push stage

✅ Add Kubernetes deployment YAML

✅ Integrate SonarQube for code quality

✅ Add Trivy or Snyk security scanning

📚 Learning Outcomes

By working on this project, you will learn:

How CI/CD pipelines work in real projects

How Java apps are containerized

How Jenkins automates builds

How DevOps tools integrate together


Sri Datta Chetan Bissati
System Engineer – TCS
DevOps & Cloud Enthusiast
