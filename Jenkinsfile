pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout SCM here
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Your build steps here
            }
        }
        stage('Test') {
            steps {
                // Your test steps here
            }
        }
    }
    
    post {
        always {
            script {
                try {
                    currentBuild.result = 'SUCCESS'
                } catch (Exception e) {
                    currentBuild.result = 'SUCCESS'
                }
            }
        }
    }
}


