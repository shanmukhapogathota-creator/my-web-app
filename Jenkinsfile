pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'dir'
            }
        }

        stage('Deploy') {
            steps {
                bat 'if not exist deployed mkdir deployed'
                bat 'copy index.html deployed'
            }
        }
    }
}
