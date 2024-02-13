pipeline {
    agent any

    triggers {
        GenericTrigger(
         genericVariables: [
          [key: 'action', value: '$.action'],
          [key: 'merged', value: '$.pull_request.merged']
         ],
         causeString: 'Triggered on $action with merge status $merged',
         printContributedVariables: true,
         printPostContent: true,
         silentResponse: false
        )
    }

    stages {
        stage('Check for Merge') {
            steps {
                script {
                    if (env.merged == 'true') {
                        echo "Pull request merged, running the pipeline..."
                        // Your pipeline steps go here
                    } else {
                        echo "Not a merge event, skipping..."
                    }
                }
            }
        }
    }
}