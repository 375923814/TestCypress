pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm run cypress'
            }
        }
        stage('Deploy') {
            steps {
                println "Deploy"
            }
        }
    }
}
