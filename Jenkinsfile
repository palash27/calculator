pipeline {
    agent any;
    environment {

    }
    tools {
        nodejs 'jenkins-demo-node'
    }
    stages {
        stage('Initialize') {
            steps {
                sh '''
                    npm install
                '''
            }
        }
        stage('Unit Tests') {
            steps {
                sh '''
                    npm run test -- --watchAll=false
                '''
            }
        }
        stage('Build') {
            steps {
                sh '''
                    npm run build
                '''
            }
        }
    }
}