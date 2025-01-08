pipeline {
    agent any

    stages {
        stage ('Checkout'){
            steps {
                sh 'git checkout $BRANCH'
                sh 'git pull origin $BRANCH'
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'npm start'
                }
            }
        }
        stage('Deploy') {
            echo 'Deploying application'
        }
    }
}