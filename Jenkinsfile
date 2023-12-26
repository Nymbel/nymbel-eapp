pipeline {
    agent {
        docker {
            image 'node:20.10.0-alpine3.19' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Install') { 
            steps {
                sh 'yarn install' 
            }
        }
        stage('Build Docker Image') { 
            steps {
                sh 'yarn docker'
                sh 'yarn pushdocker'
            }
        }

    }
}