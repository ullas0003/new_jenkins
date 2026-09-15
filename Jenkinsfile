def stage1Status = ''
pipeline {
    agent any

    stages {
        stage('STAGE1') {
            steps {
                script {
                    try {
                        sh '''
                           exit 1
                               '''
                    }catch(Exception e){
                        echo "Caught exception: ${e.message}"
                        single1Status = 'FAILED'
                    }
                }
                
            }
        }
         stage('STAGE2') {
            when{
                expression{
                    stage1Status == 'SUCCESS'
                }
            }
            steps {
                   echo "stage1 is success"
                }
        }
         stage('STAGE3') {
           when{
                expression{
                    stage1Status == 'FAILED'
                }
            }
            steps {
                
                    steps{
                     echo "stage1 is Failed"
                    }
                
                   
            }
        }
         
    }
}
