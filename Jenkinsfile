pipeline {
    agent any
    triggers {
        cron('H/10 * * * 4') // Every 10 minutes on Thursdays
    }
    stages {
        stage('Checkout SCM') {
            steps {
                
                checkout scm
            }
        }
        stage('Build') {
            steps {
                
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                
                sh 'mvn test'
            }
        }
        stage('Generate Code Coverage') {
            steps {
                sh 'mvn jacoco:report'
            }
        }
    }
}

