pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/robinthakur00/iCoderDjango.git'
            }
        }

        stage('Build Docker image') {
            steps {
                sh 'docker build -t icoder .'
            }
        }

        stage('Run Docker container') {
            steps {
                sh 'docker run -d -p 8000:8000 icoder'
            }
        }
    }
}
