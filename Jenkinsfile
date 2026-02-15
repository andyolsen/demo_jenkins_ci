pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Configure') {
            steps {
                bat 'cmake --preset ci'
            }
        }

        stage('Build') {
            steps {
                bat 'cmake --build --preset ci'
            }
        }

        stage('Test') {
            steps {
                bat 'ctest --preset ci'
            }
        }
    }
}
