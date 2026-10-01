pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checkout source code...'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'No dependencies required.'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'

                bat '''
                    if not exist index.html exit /b 1
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying website...'
            }
        }
    }

    post {
        success {
            echo 'DEPLOY SUCCESS'
        }

        failure {
            echo 'DEPLOY FAILED'
        }
    }
}