pipeline {
    agent any

    stages {
        stage ('Checkout'){
            steps {
                script {
                    sh 'git checkout $BRANCH'
                    sh 'git pull origin $BRANCH'
                }         
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
                    sh 'npm test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    echo 'Deploying application'
                }
            }
        }
    }
}