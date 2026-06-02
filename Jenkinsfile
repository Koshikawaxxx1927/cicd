pipeline {

    agent any

    stages {

        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }

        stage('Package') {
            steps {
                sh './mvnw package'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t employee-api .'
            }
        }
    }
}