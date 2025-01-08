pipeline {
    agent any

    stages {
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