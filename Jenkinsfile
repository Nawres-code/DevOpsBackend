pipeline {
    agent any

    stages {
        stage('Clean up') {
            steps {
                // Clean up workspace before starting the pipeline
                deleteDir()
            }
        }
        stage('Checkout') {
            steps {
                // Clone the GitHub repository and checkout the 'salsabilbackdevops' branch
                git url: 'https://github.com/Nawres-code/DevOpsBackend.git', branch: 'LakhalBackDevOps'
            }
        }
    }

    post {
        always {
            // Always clean the workspace after the pipeline execution
            cleanWs()
        }
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}