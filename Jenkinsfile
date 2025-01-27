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
        // stage ('SonarQube Analysis'){
        //     steps {
        //         script {
        //             def scannerHome = tool 'sonar';
        //             withSonarQubeEnv() {
        //               sh "${scannerHome}/bin/sonar-scanner"
        //             }
        //         }
        //     }
        // }
                    
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
            steps {
                script{
                    echo 'Deploying application'
                }
            }
        }
    }
}
