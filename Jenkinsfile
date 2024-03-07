pipeline {
    tools {
        nodejs "node"
    }
    agent any
    
 environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './public/test.sh'
            }
        }
        stage('Deliver') {
            steps {
                sh './public/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './public/kill.sh'
            }
        }
        }   
    }

