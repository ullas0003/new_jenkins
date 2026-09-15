pipeline {
    agent any

    stages {
        stage('STAGE1') {
            steps {
                sh '''
                   sleep 10
                '''
            }
        }
         stage('STAGE2') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE'){
                    sh '''
                   exit 1
                '''
                }
                
            }
        }
         stage('STAGE3') {
            steps {
                script{
                    try{
                         exit 1
                   sleep 5
                '''
                    } catch(Exception e) {
                        echo "Caght an Exception: ${e.message}"
                        currentBuild.result = 'SUCCESS'
                    }finally{
                        echo "Cleaning up ...."
                    }
                   
                }
                
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
