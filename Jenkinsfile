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
                cmd 'cmake --preset ci'
            }
        }

        stage('Build') {
            steps {
                cmd 'cmake --build --preset ci'
            }
        }

        stage('Test') {
            steps {
                cmd 'ctest --preset ci'
            }
        }
    }
}
