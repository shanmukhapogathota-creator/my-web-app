
pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t todo-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f todo-container || true'
                sh 'docker run -d --restart unless-stopped --name todo-container -p 8083:80 todo-app'
            }
        }

    }
}
