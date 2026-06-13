pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t todo-app .'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker rm -f todo-container || exit 0'
                bat 'docker run -d --name todo-container -p 8082:80 todo-app'
            }
        }
    }
}
