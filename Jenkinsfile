pipeline {
    agent {
        docker {
          image 'node:12.18.0-alpine'
        }
     }
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
