pipeline {
    agent {
        label 'agent-5'
    }
    stages {
        stage('STAGE1') {
            steps {
                sh '''
                    ls -ltr
                    sleep 10
                '''
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
