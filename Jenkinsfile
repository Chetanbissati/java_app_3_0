pipeline {
    agent any

    // Tools section can be optional if your agent already has Java and Maven installed in PATH
    // Otherwise, make sure the names match Jenkins Global Tool Configuration
    tools {
        jdk 'jdk-17'       // <-- Replace with your JDK name in Jenkins if different
        maven 'maven-3.9'  // <-- Replace with your Maven name in Jenkins if different
    }

    stages {
        stage('Checkout') {
            steps {
                // Pull code from GitHub
                git branch: 'main', url: 'https://github.com/Chetanbissati/java_app_3_0.git'
            }
        }

        stage('Build') {
            steps {
                // Build using Maven
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Optional: run tests
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment steps go here (e.g., copy WAR to server, run scripts)"
            }
        }
    }

    post {
        success {
            echo 'Build & Deploy Succeeded ✅'
        }
        failure {
            echo 'Build or Deploy Failed ❌'
        }
    }
}

