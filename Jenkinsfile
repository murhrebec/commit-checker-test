pipeline {
    agent any

    stages {
        stage('Changes available...') {
            steps {
                echo 'Files uploaded...'
            }
        }
        stage('No changes available...') {
            steps {
                script {
                    currentBuild.result = 'NOT_BUILT'
                }
                /*
                catchError(buildResult: 'ABORTED', stageResult: 'UNSTABLE') {
                    sh "exit 1"
                }
                */
            }
        }
    }
}
