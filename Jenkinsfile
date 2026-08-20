pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('build') {
            steps {
                bat 'docker build -t mywebsite:v1 .'
            }
        }
    }
}
