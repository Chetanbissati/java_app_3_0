pipeline {
    agent any

    tools {
        jdk 'jdk17'          // MUST exist in Jenkins Global Tool Configuration
        maven 'maven3'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Maven Clean') {
            steps {
                sh 'mvn clean'
            }
        }

        stage('Maven Build') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }
    }

    post {
        success {
            echo '✅ Spring Boot JAR built successfully'
            sh 'ls -lh target'
        }
        failure {
            echo '❌ Maven build failed'
        }
    }
}
