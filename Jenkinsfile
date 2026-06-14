pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t todo-app .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker rm -f todo-container || true'
                sh 'docker run -d --name todo-container -p 8082:80 todo-app'
            }
        }
    }
}
