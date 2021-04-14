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
                sh 'docker run -it -v $PWD:/e2e -w /e2e cypress/included:7.0.1'
                sh 'npm install'
                // sh 'npm run cypress:install'
            }
        }       
        stage('Test') {
            steps {
                sh 'npm run cypress'
            }
        }       
    }
}
