pipeline{
agent any

    stages {
        stage('STAGE1') {
            when{
                branch 'main'
            }
            steps {
                echo "${env.BUILD_NUMBER}"
                echo "${env.JOB_NAME}"
                echo "${env.GIT_BRANCH}"
                echo "${env.GIT_URL}"
            }
        }
         
         
    }
}
