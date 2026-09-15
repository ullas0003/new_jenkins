pipeline {
   agent any
   environment{
     APP = 'frontend'
     BRANCH = 'main'
   }
    stages {
        stage('STAGE1') {
            environment{
                APP = 'frontend'
            }
            steps {
                sh '''
                    echo APP - $APP
                    echo $BRANCH
                    sleep 10
                '''
            }
        }
        stage('STAGE2') {
             
            steps {
                sh '''
                    echo APP - $APP
                    echo BRANCH - $BRANCH
                    sleep 5
                    ls -lrt
                '''
            }
        }
        stage('STAGE3') {
             agent {
                  label 'agent-2'
                   }
            steps {
                echo 'This is STAGE3'
            }
        }
        stage('STAGE4') {
            agent any
            steps {
                sh 'echo This is STAGE4'
            }
        }
    }
}
