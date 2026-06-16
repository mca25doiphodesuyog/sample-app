pipeline {
    agent any

    stages {

        stage('Pull Latest Code') {
            steps {
                checkout scm
            }
        }

        stage('Run Unit Tests') {
            steps {
                sh 'pip install -r requirements.txt'
                sh 'pytest'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sample-app .'
            }
        }

        stage('Push Docker Image') {
            steps {
                echo 'Docker Hub push configured separately.'
            }
        }
    }
}