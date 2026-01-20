pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application'
                writeFile file: 'build-output.txt', text: 'Build successful'
            }
        }

        stage('Test') {
            steps {
                error 'Test failed due to low accuracy'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: '*.txt'
        }
        success {
            echo 'Pipeline completed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
