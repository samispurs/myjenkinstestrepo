pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
    post {
        always {
            echo 'ALWAYS: This will always run'
        }
        success {
            echo 'SUCCESS: This will run only if successful'
        }
        failure {
            echo 'FAILED: This will run only if failed'
        }
        unstable {
            echo 'UNSTABLE: This will run only if the run was marked as unstable'
        }
        changed {
            echo 'CHANGED: This will run only if the state of the Pipeline has changed'
            echo 'CHANGED: For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
