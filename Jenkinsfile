

pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
                echo 'Code downloaded from GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Build completed successfully'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing completed successfully'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}

