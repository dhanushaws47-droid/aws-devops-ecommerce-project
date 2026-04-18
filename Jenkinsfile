pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/dhanushaws47-droid/aws-devops-ecommerce-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-backend ./backend'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 devops-backend || true'
            }
        }
    }
}
