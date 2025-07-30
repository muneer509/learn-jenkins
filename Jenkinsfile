Here’s a simple example of a Jenkins Pipeline script written in Groovy. This script demonstrates a basic CI/CD pipeline with stages for building, testing, and deploying an application:

Copy code
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh './gradlew build' // Replace with your build command
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './gradlew test' // Replace with your test command
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh './deploy.sh' // Replace with your deployment script
            }
        }
    }

    post {
        always {
            echo 'Cleaning up workspace...'
            cleanWs()
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}

Key Points:
agent any: Specifies that the pipeline can run on any available Jenkins agent.
Stages: Each stage represents a step in the pipeline (e.g., Checkout, Build, Test, Deploy).
Post Actions: Defines actions to perform after the pipeline execution (e.g., cleanup, success, failure notifications).

You can customize this script based on your project’s requirements, such as using different build tools, test frameworks, or deployment strategies.