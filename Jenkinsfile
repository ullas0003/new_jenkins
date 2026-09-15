pipeline {
    agent {
        label 'agent-1'
    }
    stages {
        stage('STAGE1') {
            steps {
                sh 'ls -ltr'
            }
        }
        stage('STAGE2') {
            steps {
                sh '''
                    pwd
                    sleep 5
                    ls -lrt
                '''
            }
        }
        stage('STAGE3') {
            steps {
                echo 'This is STAGE3'
            }
        }
        stage('STAGE4') {
            steps {
                sh 'echo This is STAGE4'
            }
        }
    }
}
