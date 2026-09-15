pipeline {
   agent any
    parameters {
     string defaultValue: 'main', description: 'Provide the branch to build and deploy', name: 'BRANCH'
      }
    stages {
        stage('STAGE1') {
            agent any
            steps {
                sh '''
                    ls -ltr
                    sleep 10
                '''
            }
        }
        stage('STAGE2') {
             agent {
        label 'agent-1'
    }
            steps {
                sh '''
                    pwd
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
