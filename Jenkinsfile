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
                sh 'cmake --preset ci'
            }
        }

        stage('Build') {
            steps {
                sh 'cmake --build --preset ci'
            }
        }

        stage('Test') {
            steps {
                sh 'ctest --preset ci'
            }
        }
    }
}
