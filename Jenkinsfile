pipeline {
    agent any
    triggers {
        cron('H/10 * * * 4') // Every 10 minutes on Thursdays
    }
    stages {
        stage('Checkout SCM') {
            steps {
                // Checkout SCM steps here
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Build steps here
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                // Test steps here
                sh 'mvn test'
            }
        }
        stage('Generate Code Coverage') {
            steps {
                // Code coverage steps here
                sh 'mvn jacoco:report'
            }
        }
    }
}

