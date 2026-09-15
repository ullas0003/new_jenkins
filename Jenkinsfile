pipeline {
    agent any

    stages {
        stage('STAGE1') {
            steps {
                sh '''
                   exit 1
                '''
            }
        }
         stage('STAGE2') {
            steps {
                sh '''
                   sleep 5
                '''
            }
        }
         stage('STAGE3') {
            steps {
                sh '''
                   sleep 5
                '''
            }
        }
         stage('STAGE4') {
            steps {
                sh '''
                   sleep 5
                '''
            }
        }
    }
}