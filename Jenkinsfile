pipeline {
    agent {
        docker { image 'node:20.11.0-alpine3.19' }
       // always true //optional
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }

         stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run build') {
            steps {
                sh 'npm run build'
            }
    }
}
}