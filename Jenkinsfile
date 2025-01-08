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
        
        // stage('Run Tests') {
        //     steps {
        //         script {
        //             sh 'npm test'
        //         }
        //     }
        // }

        stage('Deploy') {
            steps {
                script {
                    sh 'npm start'
                }
            }
        }
    }
}