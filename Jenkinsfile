pipeline {
    agent {
        docker {
          image 'node:12.18.0-alpine'
          image 'cypress/included:6.1.0'
        }
     }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run cypress:install'
            }
        }       
        stage('Test') {
            steps {
                sh 'npm run cypress'
            }
        }       
    }
}
