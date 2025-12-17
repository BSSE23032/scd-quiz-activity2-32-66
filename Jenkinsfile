pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flaskapp:v1 app/web'
            }
        }

        stage('Test Image') {
            steps {
                sh 'echo "Docker image built successfully"'
            }
        }
                stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f kubernetes/deployment.yaml'
                sh 'kubectl apply -f kubernetes/service.yaml'
                sh 'kubectl rollout restart deployment mysite-deployment'
            }
        }
    }
}
