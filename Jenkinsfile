pipeline {
    agent any
    stages {
        stage('STAGE1') {
            when {
                expression {
                env.GIT_BRANCH == 'origin/main'   // ✅ only runs if branch is "main"
            }
            }
            steps {
                echo "BUILD_NUMBER: ${env.BUILD_NUMBER}"
                echo "JOB_NAME: ${env.JOB_NAME}"
                echo "GIT_BRANCH: ${env.GIT_BRANCH}"
                echo "GIT_URL: ${env.GIT_URL}"
            }
        }
    }
}
