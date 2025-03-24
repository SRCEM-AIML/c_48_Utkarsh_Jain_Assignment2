pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/SRCEM-AIML/c_48_Utkarsh_Jain_Assignment2.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t utkarsh2005/studentproject .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                withDockerRegistry([credentialsId: 'docker-hub-credentials', url: '']) {
                    sh 'docker push utkarsh2005/studentproject'
                }
            }
        }
    }
}
