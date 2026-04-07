pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f my-container || true'
                sh 'docker run -d -p 8081:80 --name my-container my-app'
            }
        }
    }
}
