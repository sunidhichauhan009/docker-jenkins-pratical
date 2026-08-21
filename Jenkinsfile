pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t mywebsite:v1 .'
            }
        }

        stage('docker push'){
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'sunidhi002', passwordVariable: '45sdfgh4567dcfvgh5678')]) 
                {
                    bat "docker login -u sunidhi002 -p 45sdfgh4567dcfvgh5678
                    bat 'docker push sunidhi002/mywebsite:v1'
                }
            }
        }

    }
}
  

