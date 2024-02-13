pipeline {
    agent any

    stages {
        stage('Build') {
            triggers {

            }
            when {
                allOf {
                    expression { env.GITHUB_PR_STATE == "CLOSE" }
                    expression { env.GITHUB_PR_TARGET_BRANCH == "master" }
                }
            }
            steps {
                echo 'PR was merged to master...'
            }
        }
        stage('Test') {
            steps {
                echo 'Something else happened...'
            }
        }
    }
}
