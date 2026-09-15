pipeline{
agent any

    stages {
        stage('STAGE1') {
            when{
                branch 'main'
            }
            steps {
                sh '''
                    git branch
                    '''
                echo "This is when example"
            }
        }
         
         
    }
}
