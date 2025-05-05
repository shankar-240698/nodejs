pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Run npm install or other Node.js-related tasks
                    sh 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Run build tasks like `npm run build`
                    sh 'npm run build'
                }
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
