 
org.jenkinsci.plugins.durabletask.BourneShellScript.HEARTBEAT_CHECK_INTERVAL=300

pipeline {
    agent {
        docker {
          image 'node:12.18.0-alpine'
          image 'cypress/included:7.0.1'
        }
     }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                // sh 'npm run cypress:install'
            }
        }       
        stage('Test') {
            steps {
                sh 'ls -la'
                sh 'cypress --version'
                sh 'which cypress'
                sh 'npm run cypress'               
            }
        }       
    }
}
