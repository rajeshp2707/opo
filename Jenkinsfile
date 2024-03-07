pipeline {
    agent any
    tools {
       nodejs "node"
    }
    environment {
        CI = false          
    }
    stages {
        stage('Build') {
            steps {
              echo 'asc'
            }
        }
         stage('deploy') {
            steps {
                sh 'npm install -g npm-check-updates'
                sh 'npm install -g serve'
                sh 'serve -s build'
            }
        }
        
       
    }
}
